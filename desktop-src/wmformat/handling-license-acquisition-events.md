---
title: Behandeln von Lizenz Erwerbs Ereignissen
description: Behandeln von Lizenz Erwerbs Ereignissen
ms.assetid: e118bf09-1fa6-41b6-a6bb-3e8cb6097994
keywords:
- Windows Media-Format-SDK, behandeln von Lizenz Erwerbs Ereignissen
- Windows Media-Format-SDK, Lizenz Erwerbs Ereignisse
- Advanced Systems Format (ASF), behandeln von Lizenz Erwerbs Ereignissen
- ASF (Advanced Systems Format), behandeln von Lizenz Erwerbs Ereignissen
- Advanced Systems Format (ASF), Lizenz Erwerbs Ereignisse
- ASF (Advanced Systems Format), Lizenz Erwerbs Ereignisse
- Digital Rights Management (DRM), behandeln von Lizenz Erwerbs Ereignissen
- DRM (Digital Rights Management), behandeln von Lizenz Erwerbs Ereignissen
- Digital Rights Management (DRM), Lizenz Erwerbs Ereignisse
- DRM (Digital Rights Management), Lizenz Erwerbs Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5e31fd5b108f41d5b0925918fdf1c83764bcf7e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104389884"
---
# <a name="handling-license-acquisition-events"></a>Behandeln von Lizenz Erwerbs Ereignissen

Eine DRM-fähige Reader-Anwendung in der [**iwmstatuscallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) -Rückruf Methode behandelt die folgenden vier Ereignisse im Zusammenhang mit dem Lizenz Erwerbs Vorgang:

-   **WMT \_ licengurl- \_ Signatur \_ Status**
-   **WMT \_ keine \_ Rechte**
-   **WMT \_ keine \_ Rechte \_ Ex**
-   **WMT-Abruf \_ \_ Lizenz**

**WMT \_ licengurl- \_ Signatur \_ Status**

Wenn von der DRM-Komponente Inhalte erkannt werden, die von DRM-Version 7 geschützt werden, wird zuerst nach einer gültigen Lizenz auf dem lokalen System gesucht. Wenn keines vorhanden ist, wertet es die Lizenz Erwerbs-URL im DRM-Header der Datei aus und sendet ein **WMT \_ licenseurl- \_ Signatur \_ Zustands** Ereignis mit *pValue* , das auf einen der [**WMT- \_ drmla- \_ Vertrauensstellungs**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_drmla_trust) Werte festgelegt ist und angibt, ob die URL vertrauenswürdig oder nicht vertrauenswürdig ist oder manipuliert wurde. Wenn die URL nicht vertrauenswürdig ist, sollte die Anwendung den Benutzer warnen. Wenn die URL manipuliert wurde, sollte die Datei als beschädigt angesehen werden, und die Anwendung sollte nicht zur URL navigieren, ohne dass eine Warnung für den Benutzer ausgegeben wird.

**WMT \_ keine \_ Rechte**

Das Ereignis **WMT \_ No \_ Rights** wird nur für den Inhalt der DRM-Version 1 gesendet, was bedeutet, dass die Lizenz nicht im Hintergrund erworben werden muss. Das heißt, der Benutzer muss zu einer Webseite navigieren, um eine Lizenz zu erhalten. Die URL für die Seite wird als breit Zeichen-NULL-terminierte Zeichenfolge aus dem *pValue* -Parameter in der **OnStatus** -Methode abgerufen.

Wenn dies der Fall ist, kann eine Anwendung die Navigation zu der Webseite vereinfachen, indem Sie entweder Internet Explorer in einem separaten Prozess öffnen oder das WebBrowser-Steuerelement als Host verwenden. Dies ist jedoch nicht erforderlich. Mindestens eine Anwendung könnte einfach die URL für den Benutzer in einem Meldungs Feld anzeigen und Sie auffordern, Sie in die Adressleiste von Internet Explorer einzufügen. Das Audioplayer-Beispiel veranschaulicht die ordnungsgemäße Behandlung des **WMT-Ereignisses \_ ohne \_ Rechte** , einschließlich der Formatierung der URL-Zeichenfolge und der Verwendung **der Methode "** Methode", um Internet Explorer zu öffnen und zur angegebenen URL zu navigieren.

Da die Anwendung nicht weiß, wann eine DRM-Lizenz der Version 1 abgerufen wurde, kann der Benutzer versuchen, die Datei nach dem Erwerb der Lizenz erneut zu öffnen.

Dieser nicht automatische Lizenz Erwerbsprozess kann auch für Lizenzen der Version 7 verwendet werden. in diesem Fall kann die Anwendung jedoch zuerst [**iwmdrmreader:: monitorlicenseacquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-monitorlicenseacquisition)anrufen. Diese Methode bewirkt, dass der lokale Lizenz Speicher wiederholt geprüft wird, bis die Lizenz für die neue Datei gefunden wird. An diesem Punkt empfängt die Anwendung ein **WMT-Abruf \_ \_ Lizenz** Ereignis. Für alle Lizenzen der Version 7 empfiehlt es sich, dass Anwendungen Benutzern die Option zum automatischen Abrufen von Lizenzen oder nicht im Hintergrund zukommen lassen.

**WMT \_ keine \_ Rechte \_ Ex**

Das Ereignis **WMT \_ No \_ Rights \_ Ex** gibt an, dass der Inhalt durch DRM-Version 7 geschützt ist. Daher kann der Lizenz Erwerbsprozess entweder unbeaufsichtigt oder nicht im Hintergrund fortgesetzt werden. Im Allgemeinen ist der automatische Erwerb von Lizenzen für Endbenutzer bequemer, auch wenn es für einige Benutzer vorzuziehen ist, alle Lizenzen nicht im Hintergrund zu erwerben. Wenn der Lizenzerwerb erfordert, dass der Benutzer Zahlungs-oder persönliche Informationen sendet, sollte der Prozess immer ohne Hintergrund ausgeführt werden. Der nicht automatische Lizenzerwerb wird oben unter der Überschrift " **WMT \_ No \_ Rights** " beschrieben. Der automatische Erwerb erfolgt wie folgt:

1.  Wandeln Sie den *pValue* -Parameter in eine [**WM- \_ \_ Lizenz \_ Daten**](wm-get-license-data.md) Struktur um, und speichern Sie die Struktur für den Fall, dass Sie später für den nicht automatischen Lizenzerwerb benötigt wird.
2.  Rufen Sie **QueryInterface** für das Reader-Objekt auf, um die [**iwmdrmreader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) -Schnittstelle zu erhalten.
3.  Nennen Sie [**iwmdrmreader:: AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) , und geben Sie im *dwFlags* -Parameter 0x1 an, um den automatischen Abruf der Sprache anzugeben. Dies ist ein asynchroner Rückruf, der sofort zurückgegeben wird.
4.  Warten Sie, bis das **WMT- \_ \_ Lizenz** Ereignis abgerufen wurde.

**WMT-Abruf \_ \_ Lizenz**

Das **WMT \_ \_** -Ereignis zum Abrufen einer Lizenz wird gesendet, nachdem der Lizenz Erwerbs Vorgang für eine DRM-Lizenz Version 7 abgeschlossen wurde. [**Iwmdrmreader:: AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) bewirkt, dass dieses Ereignis für die automatische Übernahme gesendet wird, und [**monitorlicenseacquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-monitorlicenseacquisition) bewirkt, dass es für einen nicht automatischen Erwerb gesendet wird. Wandeln Sie in Ihrem Ereignishandler *pValue* in einen Zeiger auf eine [**WM-Lizenz für die \_ \_ Lizenz \_ Daten**](wm-get-license-data.md) Struktur um, und untersuchen Sie das **HR** -Element, um zu bestimmen, ob die Lizenz erfolgreich abgerufen wurde. Wenn **HR** dem NS \_ E \_ DRM \_ keine \_ Rechte zuweist, weist dies darauf hin, dass die Lizenz nicht im Hintergrund erworben werden muss. Anwendungen sollten es Benutzern ermöglichen, den Lizenz Erwerbsprozess jederzeit abzubrechen. Dies erfolgt durch Aufrufen von [**iwmdrmreader:: cancellicenabacquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-cancellicenseacquisition). Wenn Sie diese Methode aufrufen, wird ein **WMT-Abruf \_ \_ Lizenz** Ereignis mit einem **HRESULT** -Wert des NS-DRM-Abruf Abrufs gesendet \_ \_ \_ \_ .

Wenn **HR** gleich \_ \_ \_ \_ der erworbenen NS-DRM-Lizenz ist, wurde die Lizenz abgerufen, und die Anwendung kann versuchen, die Datei wiederzugeben oder Sie auf ein Gerät zu kopieren oder eine beliebige Aktion auszuführen, für die Sie Rechte angefordert hat.

Unter Windows XP wurde ein neuer Fehlercode eingeführt: NS \_ E \_ DRM- \_ Lizenz \_ noterworben. Dieser Fehlercode wird generiert, wenn die Laufzeitkomponenten des Windows Media-Formats unter Windows XP während des automatischen oder nicht automatischen Lizenz Erwerbs keine Lizenz erhalten. Auf anderen Plattformen \_ \_ wird der NS E DRM- \_ Lizenz \_ Speicher \_ Fehler normalerweise zurückgegeben, wenn der Lizenzerwerb fehlschlägt. Mit dem neuen Fehlercode soll der Lizenz Erwerbs Fehler von anderen Fehlerbedingungen unterschieden werden, bei denen der Fehler "NS \_ E \_ DRM- \_ Lizenz \_ Speicher" \_ generiert wird.

Die empfohlene Methode, diese Fehler zu behandeln, wenn Sie nach einem automatischen Lizenz Erwerbs Versuch zurückgegeben wird, wird im folgenden Code Ausschnitt gezeigt:


```C++
if( hrStatus == NS_E_DRM_LICENSE_NOTACQUIRED || 
    hrStatus == NS_E_DRM_LICENSE_STORE_ERROR )
{
  // Attempt non-silent license acquisition.
}
else if( hrStatus == NS_E_DRM_NEEDS_INDIVIDUALIZATION )
{
  // Individualize and then retry.
}
else if( FAILED(hrStatus) )
{
  // Display a helpful error message.
}
else
{
  // Success. Play content.
}
```



> [!Note]  
> DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Geschützte Dateien werden gelesen.**](reading-protected-files.md)
</dt> </dl>

 

 




