---
title: URIs in Windows 8.1
description: Windows 8.1 sind nur HTTPS-URIs und keine HTTP-URIs möglich.
ms.assetid: 06BDD3A3-67B7-4085-83DA-F322F718C876
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3246cad0fb6114a3a01d781ed990e0c277547e2b9ee489572c8124a23e7e81b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028808"
---
# <a name="windows-81-allows-only-https-uris-not-http-uris"></a>Windows 8.1 sind nur HTTPS-URIs und keine HTTP-URIs möglich.

## <a name="platforms"></a>Plattformen

<dl> Clients – Windows 8.1  
Server – Windows Server 2012 R2  
</dl>

## <a name="description"></a>Beschreibung

Apps, die für Windows 8 können http- und https-URIs in ihre Anwendungsinhalts-URIs enthalten, apps, die für Windows 8.1 erstellt wurden, enthalten möglicherweise nur HTTPS-URIs.

Die einzige Ausnahme ist für dynamische ContentUriRules, die in der AppxManifest.xml der App angegeben sind. Mit dynamischen ContentUriRules können Apps auf zusätzliche Domänen oder Netzwerkressourcen zugreifen, die vom Administrator bereitgestellt werden, z. B. Gruppenrichtlinie URIs. Dynamische ContentUriRules sind jedoch nur für Windows Store verfügbar, wenn sie die folgenden Bedingungen erfüllen:

-   Die Gruppenrichtlinie ist aktiviert.
-   Das Paket hat die enterpriseAuthentication-Funktion angegeben.
-   OsMaxVersionTested des Pakets ist Windows 8.1 oder höher.

Die neuen Einschränkungen in Windows 8.1 sind Teil der erweiterten Sicherheitseinschränkungen, um die Plattform weiter zu schützen.

## <a name="manifestations"></a>Manifestationen

Beim Ausführen einer App, die für Windows 8 auf Windows 8.1 erstellt wurde, ist die Verwendung von HTTP-URIs in [ApplicationContentUriRules](/uwp/schemas/appxpackage/appxmanifestschema/element-applicationcontenturirules) zulässig.

## <a name="mitigations"></a>Gegenmaßnahmen

Es wird empfohlen, dass WWA-Entwickler von zum [<iframe>](https://msdn.microsoft.com/library/windows/apps/hh465955.aspx) [WebView-Steuerelement](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041) wechseln (<x-ms-webview->). Wenn Sie jedoch Unterstützung für Den Zugriff auf AppCache, IndexedDB, Geolocation oder programmgesteuerte Zwischenablage benötigen, müssen Sie weiterhin verwenden. <iframe> für Windows 8.1.

Fortgesetzte Verwendung von <iframe> für Remoteinhalte ist ein neuer Eintrag in ApplicationContentUriRules für die App erforderlich. Apps mit WebView erfordern neue Einträge in ApplicationContentUriRules, wenn der Webinhalt window.external.notify zum Generieren eines [ScriptNotify-Ereignisses aufrufen](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041) muss. Wenn Sie nicht über Visual Studio verfügen, können Sie das App-Manifest aktualisieren, indem Sie den folgenden XML-Code hinzufügen, einschließlich Platzhaltern für Unterdomänen (z. B. https:// \* .microsoft.com):


```
<Package>
    …
    <Applications>
        <Application>
            …
            <ApplicationContentUriRules>
                <Rule Match="https://www.example.com" Type="include"/>
            </ApplicationContentUriRules>
        </Application>
    </Applications>
</Package>
```



## <a name="resources"></a>Ressourcen

-   [ApplicationContentUriRules](/uwp/schemas/appxpackage/appxmanifestschema/element-applicationcontenturirules)
-   [<iframe>\| <iframe> Elementobjekt](https://msdn.microsoft.com/library/windows/apps/hh465955.aspx)
-   [Webview-Klasse](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041)
-   [WebView.ScriptNotify-Ereignis](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041)

 

 