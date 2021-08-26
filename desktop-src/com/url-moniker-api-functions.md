---
title: URL-Monikerfunktionen
description: URL-Monikerfunktionen
ms.assetid: 773743d3-9434-4ec9-b85c-9b971e37682f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd4dc19d47a933e9f93516630b25fdab2f64b21cb3755ac9fd5bbdfa7edaba51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992040"
---
# <a name="url-moniker-functions"></a>URL-Monikerfunktionen

URL-Monikerfunktionen isolieren Entwickler von der Komplexität beim Erstellen, Verwalten und Verwenden von URL-Monikern. Diese Funktionen lauten wie folgt:

-   [**CreateURLMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775102(v=vs.85))
-   [**IsValidURL**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775112(v=vs.85))
-   [**RegisterMediaTypes**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775118(v=vs.85))
-   [**CreateFormatEnumerator**](/windows/desktop/api/Urlmon/nf-urlmon-createformatenumerator)
-   [**RegisterFormatEnumerator**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775116(v=vs.85))
-   [**RevokeFormatEnumerator**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775121(v=vs.85))
-   [**RegisterMediaTypeClass**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775117(v=vs.85))
-   [**FindMediaTypeClass**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775106(v=vs.85))
-   [**GetClassFileOrMime**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775108(v=vs.85))
-   [**UrlMkSetSessionOption**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775125(v=vs.85))

Ihre Vertrautheit mit diesen Funktionen kann wie folgt lauten:

-   Machen Sie sich [**mit CreateURLMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775102(v=vs.85)) und [**IsValidURL**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775112(v=vs.85)) vertraut, wenn Sie URL-Moniker in eigenständigen Anwendungen verwenden. Wenn Sie ein ActiveX erstellen, sollten Sie [**IBindHost::CreateMoniker anstelle**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775075(v=vs.85)) von **CreateURLMoniker verwenden.**
-   Machen Sie sich mit [**RegisterMediaTypes,**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775118(v=vs.85)) [**CreateFormatEnumerator,**](/windows/desktop/api/Urlmon/nf-urlmon-createformatenumerator) [**RegisterFormatEnumerator**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775116(v=vs.85))und [**RevokeFormatEnumerator**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775121(v=vs.85)) vertraut, wenn Sie MIME-Aushandlung mit URL-Monikern ausführen.
-   Machen Sie sich nur dann mit [**RegisterMediaTypeClass,**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775117(v=vs.85)) [**FindMediaTypeClass,**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775106(v=vs.85)) [**GetClassFileOrMime**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775108(v=vs.85))und [**UrlMkSetSessionOption**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775125(v=vs.85)) vertraut, wenn Sie sowohl mit URL-Monikern als auch mit COM über erhebliche Erfahrung verfügen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[URL-Moniker](url-monikers.md)
</dt> </dl>

 

 