export default async function handler(req, res) {
  if (req.method !== 'POST') {
    return res.status(405).json({ error: 'Method not allowed' });
  }

  const { verdict, score, details } = req.body;

  const RESEND_API_KEY = "re_isfsJGqd_MWZGJFk4nEijk2Ub2Mm7JAyH";
  const TARGET_EMAIL = "pugazhenthinadarajan@gmail.com";

  try {
    const response = await fetch('https://api.resend.com/emails', {
      method: 'POST',
      headers: {
        'Authorization': `Bearer ${RESEND_API_KEY}`,
        'Content-Type': 'application/json',
      },
      body: JSON.stringify({
        from: 'onboarding@resend.dev',
        to: TARGET_EMAIL,
        subject: `[Sister Quiz Report] Score: ${score}/25 - ${verdict}`,
        html: `
          <div style="font-family: Arial, sans-serif; padding: 20px; line-height: 1.5;">
            <h2 style="color: #db2777;">Sister Importance Verification Report 📊</h2>
            <p><strong>Verdict:</strong> ${verdict}</p>
            <p><strong>Score:</strong> ${score} / 25</p>
            <hr style="border: 0; border-top: 1px solid #eee; margin: 15px 0;">
            <h3 style="color: #4f46e5;">Detailed Selections:</h3>
            <pre style="background: #f4f4f5; padding: 12px; border-radius: 6px; font-family: monospace; white-space: pre-wrap;">${details}</pre>
          </div>
        `,
      }),
    });

    const data = await response.json();

    if (!response.ok) {
      console.error('Resend API Error:', data);
      return res.status(response.status).json({ error: data });
    }

    return res.status(200).json({ success: true, data });
  } catch (error) {
    console.error('Server Handler Error:', error);
    return res.status(500).json({ error: error.message });
  }
}
