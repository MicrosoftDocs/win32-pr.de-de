---
title: Behandeln von Lizenzerwerbsereignissen
description: Behandeln von Lizenzerwerbsereignissen
ms.assetid: e118bf09-1fa6-41b6-a6bb-3e8cb6097994
keywords:
- Windows Medienformat-SDK, Behandeln von Lizenzerwerbsereignissen
- Windows Medienformat-SDK, Lizenzerwerbsereignisse
- Advanced Systems Format (ASF), Behandeln von Lizenzerwerbsereignissen
- ASF (Advanced Systems Format), Behandeln von Lizenzerwerbsereignissen
- Advanced Systems Format (ASF), Lizenzerwerbsereignisse
- ASF (Advanced Systems Format), Lizenzerwerbsereignisse
- Digital Rights Management (DRM), Behandeln von Lizenzerwerbsereignissen
- DRM (Digital Rights Management),Behandeln von Lizenzerwerbsereignissen
- Digital Rights Management (DRM), Lizenzerwerbsereignisse
- DRM (Digital Rights Management), Lizenzerwerbsereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff7eab9afe85d4e58ae422134e5268c5b411058cf5048f774994b0cc02b173fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006710"
---
# <a name="handling-license-acquisition-events"></a>Behandeln von Lizenzerwerbsereignissen

Eine DRM-fähige Readeranwendung verarbeitet in ihrer [**IWMStatusCallback::OnStatus-Rückrufmethode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) die folgenden vier Ereignisse im Zusammenhang mit dem Lizenzerwerbsprozess:

-   **WMT \_ LICENSEURL \_ SIGNATURE \_ STATE**
-   **WMT \_ NO \_ RIGHTS**
-   **WMT \_ NO \_ RIGHTS \_ EX**
-   **WMT \_ ERWERBEN \_ EINER LIZENZ**

**WMT \_ LICENSEURL \_ SIGNATURE \_ STATE**

Wenn die DRM-Komponente durch DRM Version 7 geschützte Inhalte erkennt, sucht sie zunächst nach einer gültigen Lizenz auf dem lokalen System. Wenn keines vorhanden ist, wertet sie die Lizenzerwerbs-URL im DRM-Header der Datei aus und sendet ein **WMT \_ LICENSEURL \_ SIGNATURE \_ STATE-Ereignis** mit *pValue,* das auf einen der [**WMT \_ DRMLA \_ TRUST-Werte**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_drmla_trust) festgelegt ist, und gibt an, ob die URL vertrauenswürdig ist, nicht vertrauenswürdig ist oder manipuliert wurde. Wenn die URL nicht vertrauenswürdig ist, sollte die Anwendung den Benutzer warnen. Wenn die URL manipuliert wurde, sollte die Datei als beschädigt betrachtet werden, und die Anwendung sollte nicht zur URL navigieren, ohne eine starke Warnung für den Benutzer auszugeben.

**WMT \_ NO \_ RIGHTS**

Das **WMT \_ NO \_ RIGHTS-Ereignis** wird nur für DRM-Inhalte der Version 1 gesendet. Dies bedeutet, dass die Lizenz nicht im Hintergrund erworben werden muss. Anders ausgedrückt: Der Benutzer muss zu einer Webseite navigieren, um eine Lizenz zu erhalten. Die URL für die Seite wird als breitzeichenweise auf NULL endende Zeichenfolge aus dem *pValue-Parameter* in der **OnStatus-Methode** abgerufen.

Bei Bedarf kann eine Anwendung es dem Benutzer erleichtern, zur Webseite zu navigieren, indem sie entweder Internet Explorer in einem separaten Prozess öffnet oder das Webbrowser-Steuerelement hostet. Dies ist jedoch nicht erforderlich. Zumindest könnte eine Anwendung dem Benutzer einfach die URL in einem Meldungsfeld anzeigen und ihn auffordern, ihn in die Adressleiste von Internet Explorer einzufügen. Das Audioplayer-Beispiel veranschaulicht die ordnungsgemäße Behandlung des **WMT \_ NO RIGHTS-Ereignisses, \_** einschließlich der Formatierung der URL-Zeichenfolge und der Verwendung der **CreateProcess-Methode,** um Internet Explorer zu öffnen und zur angegebenen URL zu navigieren.

Da die Anwendung nicht wissen kann, wann eine DRM-Lizenz der Version 1 erworben wurde, kann der Benutzer versuchen, die Datei nach dem Erwerb der Lizenz erneut zu öffnen.

Dieser unbeaufsichtigten Lizenzerwerbsprozess kann auch für Lizenzen der Version 7 verwendet werden, aber in diesem Fall kann die Anwendung zuerst [**IWMDRMReader::MonitorLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-monitorlicenseacquisition)aufrufen. Diese Methode bewirkt, dass der lokale Lizenzspeicher wiederholt überprüft wird, bis die Lizenz für die neue Datei gefunden wird. An diesem Punkt empfängt die Anwendung ein **WMT \_ ACQUIRE \_ LICENSE-Ereignis.** Für alle Lizenzen der Version 7 wird empfohlen, dass Anwendungen Benutzern die Möglichkeit geben, Lizenzen unbeaufsichtigt oder nicht unbeaufsichtigt abzurufen.

**WMT \_ NO \_ RIGHTS \_ EX**

Das **WMT \_ NO RIGHTS \_ \_ EX-Ereignis** gibt an, dass der Inhalt durch DRM Version 7 geschützt ist. Daher kann der Lizenzerwerbsprozess entweder im Hintergrund oder nicht im Hintergrund fortgesetzt werden. Im Allgemeinen ist der automatische Lizenzerwerb für Endbenutzer praktischer, obwohl einige Benutzer es vorziehen, alle Lizenzen nicht im Hintergrund zu erwerben. Wenn der Lizenzerwerb erfordert, dass der Benutzer Zahlungs- oder persönliche Informationen übermittelt, sollte der Prozess immer nicht im Hintergrund ausgeführt werden. Der nicht automatische Lizenzerwerb wird oben unter der Überschrift **WMT \_ NO \_ RIGHTS** beschrieben. Die unbeaufsichtigten Übernahmen werden wie folgt fortgesetzt:

1.  Umwandlung des *pValue-Parameters* in eine [**WM GET LICENSE \_ \_ \_ DATA-Struktur**](wm-get-license-data.md) und Speichern der Struktur für den Fall, dass sie später für den nicht automatischen Lizenzerwerb benötigt wird.
2.  Rufen Sie **QueryInterface** für das Readerobjekt auf, um die [**IWMDRMReader-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) abzurufen.
3.  Rufen Sie [**IWMDRMReader::AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) auf, und geben Sie 0x1 im *dwFlags-Parameter* an, um den automatischen Spracherwerb anzugeben. Dies ist ein asynchroner Aufruf, der sofort zurückgegeben wird.
4.  Warten Sie auf das **WMT \_ ACQUIRE \_ LICENSE-Ereignis.**

**WMT \_ ERWERBEN \_ EINER LIZENZ**

Das **WMT \_ ACQUIRE \_ LICENSE-Ereignis** wird gesendet, nachdem der Lizenzerwerbsprozess für eine DRM-Lizenz der Version 7 abgeschlossen wurde. [**IWMDRMReader::AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) bewirkt, dass dieses Ereignis für den automatischen Erwerb gesendet wird, und [**MonitorLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-monitorlicenseacquisition) bewirkt, dass es für den nicht automatischen Erwerb gesendet wird. Stellen Sie in Ihrem Ereignishandler *pValue* in einen Zeiger auf eine [**WM GET LICENSE \_ \_ \_ DATA-Struktur**](wm-get-license-data.md) um, und untersuchen Sie das **hr-Element,** um zu ermitteln, ob die Lizenz erfolgreich erworben wurde. Wenn **hr** gleich NS \_ E \_ DRM NO RIGHTS \_ \_ ist, bedeutet dies, dass die Lizenz nicht im Hintergrund erworben werden muss. Anwendungen sollten es Benutzern ermöglichen, den Lizenzerwerbsprozess jederzeit abzubrechen. Dazu wird [**IWMDRMReader::CancelLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-cancellicenseacquisition)aufgerufen. Wenn Sie diese Methode aufrufen, wird ein **WMT \_ ACQUIRE \_ LICENSE-Ereignis** mit dem **HRESULT-Wert** NS \_ S \_ DRM ACQUIRE \_ \_ CANCELLED gesendet.

Wenn **hr** gleich NS \_ S \_ DRM LICENSE ACQUIRED \_ \_ ist, wurde die Lizenz erworben, und die Anwendung kann versuchen, die Datei wiederzuspielen, sie auf ein Gerät zu kopieren oder eine aktion auszuführen, für die sie Rechte angefordert hat.

Auf Windows XP wurde ein neuer Fehlercode eingeführt: NS \_ E \_ DRM \_ LICENSE \_ NOTACQUIRED. Dieser Fehlercode wird generiert, wenn die Windows Media Format-Laufzeitkomponenten auf Windows XP während des automatischen oder nicht automatischen Lizenzerwerbs keine Lizenz erwerben. Auf anderen Plattformen wird \_ NS E \_ DRM \_ LICENSE STORE ERROR in der Regel \_ \_ zurückgegeben, wenn der Lizenzerwerb fehlschlägt. Der neue Fehlercode soll lizenzerwerbsfehler von anderen Fehlerbedingungen unterscheiden, bei denen NS \_ E \_ DRM \_ LICENSE STORE ERROR \_ generiert \_ wird.

Die empfohlene Vorgehensweise zum Behandeln dieser Fehler, wenn sie nach einem unbeaufsichtigten Lizenzerwerbsversuch zurückgegeben werden, wird im folgenden Codeausschnitt gezeigt:


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

[**Lesen von geschützten Dateien**](reading-protected-files.md)
</dt> </dl>

 

 




