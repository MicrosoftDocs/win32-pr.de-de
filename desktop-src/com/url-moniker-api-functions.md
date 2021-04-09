---
title: URL-monikerfunktionen
description: URL-monikerfunktionen
ms.assetid: 773743d3-9434-4ec9-b85c-9b971e37682f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2db726d8ce6a101b0b97fbe2128e074ee5e892e3
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103858500"
---
# <a name="url-moniker-functions"></a>URL-monikerfunktionen

URL-monikerfunktionen isolieren Entwickler vor den Komplexitäten zum Erstellen, verwalten und Verwenden von URL-Monikern. Diese Funktionen lauten wie folgt:

-   [**"Kreateurlmoniker"**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775102(v=vs.85))
-   [**IsValidURL**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775112(v=vs.85))
-   [**Register mediatypes**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775118(v=vs.85))
-   [**"Kreateformatenumerator"**](/windows/desktop/api/Urlmon/nf-urlmon-createformatenumerator)
-   [**Registerformatenumerator**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775116(v=vs.85))
-   [**Revokeformatenumerator**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775121(v=vs.85))
-   [**Registermediatypeclass**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775117(v=vs.85))
-   [**Findmediatypeclass**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775106(v=vs.85))
-   [**Getclassfileormime**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775108(v=vs.85))
-   [**Urlmksesessionoption**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775125(v=vs.85))

Diese Funktionen können wie folgt aussehen:

-   Wenn Sie URL-Moniker in eigenständigen Anwendungen verwenden, sollten Sie sich mit " [**kreateurlmoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775102(v=vs.85)) " und " [**IsValidURL**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775112(v=vs.85)) " vertraut machen. Wenn Sie ein ActiveX-Steuerelement erstellen, sollten Sie [**ibindhost:: aufatemoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775075(v=vs.85)) anstelle von " **kreateurlmoniker**" verwenden.
-   Wenn Sie eine MIME-Aushandlung mit URL-Monikern ausführen, können Sie sich mit [**registermediatypes**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775118(v=vs.85)), [**kreateformatenumerator**](/windows/desktop/api/Urlmon/nf-urlmon-createformatenumerator), [**registerformatenumerator**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775116(v=vs.85))und [**revokeformatenumerator**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775121(v=vs.85)) vertraut machen.
-   Machen Sie sich mit [**registermediatypeclass**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775117(v=vs.85)), [**findmediatypeclass**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775106(v=vs.85)), [**getclassfileormime**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775108(v=vs.85))und [**urlmksesessionoption**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775125(v=vs.85)) vertraut, wenn Sie sowohl mit URL-Monikern als auch mit com eine bedeutende Umgebung haben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[URL-Moniker](url-monikers.md)
</dt> </dl>

 

 