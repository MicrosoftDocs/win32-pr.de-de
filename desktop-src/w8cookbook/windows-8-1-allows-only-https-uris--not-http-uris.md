---
title: URIs in Windows 8.1
description: Windows 8.1 lässt nur HTTPS-URIs zu, nicht HTTP-URIs.
ms.assetid: 06BDD3A3-67B7-4085-83DA-F322F718C876
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 022485f9fc5dc2657127f7bae49127e0bd3b5954
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886112"
---
# <a name="windows-81-allows-only-https-uris-not-http-uris"></a>Windows 8.1 lässt nur HTTPS-URIs zu, nicht HTTP-URIs.

## <a name="platforms"></a>Plattformen

<dl> Clients – Windows 8.1  
Server – Windows Server 2012 R2  
</dl>

## <a name="description"></a>Beschreibung

Während Apps, die für Windows 8 erstellt wurden, HTTP- und HTTPS-URIs in ihren Anwendungsinhalts-URIs enthalten können, enthalten Apps, die für Windows 8.1 erstellt wurden, möglicherweise nur HTTPS-URIs.

Die einzige Ausnahme gilt für dynamische ContentUriRules, die in der AppxManifest.xml-Datei der App angegeben sind. Mit dynamischen ContentUriRules können Apps auf zusätzliche Domänen oder Netzwerkressourcen zugreifen, die vom Administrator bereitgestellt werden, z. B. Gruppenrichtlinie URIs. Dynamische ContentUriRules sind jedoch nur für Windows Store Apps verfügbar, wenn sie diese Bedingungen erfüllen:

-   Die Gruppenrichtlinie ist aktiviert.
-   Das Paket hat die enterpriseAuthentication-Funktion angegeben.
-   OSMaxVersionTested des Pakets ist Windows 8.1 oder höher.

Die neuen Einschränkungen in Windows 8.1 sind Teil der erweiterten Sicherheitseinschränkungen zum weiteren Schutz der Plattform.

## <a name="manifestations"></a>Manifestationen

Beim Ausführen einer App, die für Windows 8 auf Windows 8.1 erstellt wurde, ist die Verwendung von HTTP-URIs in [ApplicationContentUriRules](/uwp/schemas/appxpackage/appxmanifestschema/element-applicationcontenturirules) zulässig.

## <a name="mitigations"></a>Gegenmaßnahmen

Es wird empfohlen, dass WWA-Entwickler von [<iframe>](https://msdn.microsoft.com/library/windows/apps/hh465955.aspx) zum [WebView-Steuerelement](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041) wechseln ( &lt; x-ms-webview &gt; ). Wenn Sie jedoch Unterstützung für AppCache, IndexedDB, Geolocation oder programmgesteuerten Zugriff auf die Zwischenablage benötigen, müssen Sie weiterhin verwenden. <iframe> für Windows 8.1.

Fortgesetzte Verwendung von <iframe> für Remoteinhalte erfordert einen neuen Eintrag in applicationContentUriRules für die App. Apps mit WebView erfordern neue Einträge in ApplicationContentUriRules, wenn der Webinhalt window.external.notify aufrufen muss, um ein [ScriptNotify-Ereignis](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041) zu generieren. Wenn Sie nicht über Visual Studio verfügen, können Sie das App-Manifest aktualisieren, indem Sie den folgenden XML-Code hinzufügen, einschließlich Platzhaltern für Unterdomänen (z. B. https:// \* .microsoft.com):


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

 

 
