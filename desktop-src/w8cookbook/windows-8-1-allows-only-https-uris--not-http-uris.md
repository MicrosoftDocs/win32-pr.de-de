---
title: URIs in Windows 8.1
description: Windows 8.1 nur HTTPS-URIs und keine http-URIs zulässt.
ms.assetid: 06BDD3A3-67B7-4085-83DA-F322F718C876
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 994780798bfe7ada0d7dc49794deb284e30f1605
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390857"
---
# <a name="windows-81-allows-only-https-uris-not-http-uris"></a>Windows 8.1 nur HTTPS-URIs und keine http-URIs zulässt.

## <a name="platforms"></a>Plattformen

<dl> Clients-Windows 8.1  
Server-Windows Server 2012 R2  
</dl>

## <a name="description"></a>BESCHREIBUNG

Apps, die für Windows 8 erstellt wurden, können http-und HTTPS-URIs in Ihre Anwendungsinhalts-URIs einschließen. für Windows 8.1 erstellten apps dürfen jedoch nur HTTPS-URIs enthalten.

Die einzige Ausnahme ist für dynamische contenturirules, die in der AppxManifest.xml Datei der APP angegeben werden. Mit dynamischen contenturirules-Regeln können apps auf zusätzliche Domänen oder Netzwerkressourcen zugreifen, die vom Administrator bereitgestellt werden, z. b. Gruppenrichtlinie URIs. Dynamische contenturirules sind jedoch nur für Windows Store-Apps verfügbar, wenn Sie die folgenden Bedingungen erfüllen:

-   Der Gruppenrichtlinie ist aktiviert.
-   Das Paket hat die enterprisauthentication-Funktion angegeben.
-   Osmaxversiongetesteten des Pakets ist Windows 8.1 oder höher

Die neuen Einschränkungen in Windows 8.1 sind Teil der verbesserten Sicherheitseinschränkungen, um die Plattform weiter zu schützen.

## <a name="manifestations"></a>Kundgebungen

Beim Ausführen einer APP, die für Windows 8 auf Windows 8.1 erstellt wurde, ist die Verwendung von http-URIs in den [applicationcontenturirules](/uwp/schemas/appxpackage/appxmanifestschema/element-applicationcontenturirules) zulässig.

## <a name="mitigations"></a>Gegenmaßnahmen

Es wird empfohlen, dass WWA-Entwickler von [<iframe>](https://msdn.microsoft.com/library/windows/apps/hh465955.aspx) zum [WebView](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041) -Steuerelement wechseln (<x-ms-WebView>). Wenn Sie jedoch Unterstützung für AppCache, indexeddb, Geolokation oder programmatischen Zugriff auf die Zwischenablage benötigen, müssen Sie weiterhin verwenden. <iframe> für Windows 8.1.

Fortgesetzte Verwendung von <iframe> für Remote Inhalte ist in den applicationcontenturirules-Funktionen für die APP ein neuer Eintrag erforderlich. Apps mit WebView erfordern neue Einträge in applicationcontenturirules, wenn der Webinhalt Window. extern. Notify zum Erstellen eines [scriptnotify](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041) -Ereignisses aufrufen muss. Wenn Sie nicht über Visual Studio verfügen, können Sie das App-Manifest aktualisieren, indem Sie den folgenden XML-Code hinzufügen, einschließlich der Platzhalter für Unterdomänen (z. b. https:// \* . Microsoft.com):


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
-   [<iframe> Element- \| <iframe> Objekt](https://msdn.microsoft.com/library/windows/apps/hh465955.aspx)
-   [WebView-Klasse](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041)
-   [WebView. scriptnotify-Ereignis](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041)

 

 