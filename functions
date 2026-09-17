export async function onRequest(context) {
  const { params, env } = context;
  const slug = params.slug;
  const linkLargo = await env.KV.get('link:' + slug);
  if (linkLargo) {
    return Response.redirect(linkLargo, 302);
  }
  return Response.redirect('https://guia-lara.pages.dev', 302);
}
