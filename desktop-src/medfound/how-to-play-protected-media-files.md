---
description: Abspielen von Dateien, die von DRM geschützte Medien enthalten.
ms.assetid: 85d98f49-8af2-42ce-9b36-a025aee93f73
title: Wiedergeben geschützter Mediendateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0f8f7af78881e43f2f7f85e8f333ab31b1bc2de
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106364288"
---
# <a name="how-to-play-protected-media-files"></a>Wiedergeben geschützter Mediendateien

Eine geschützte Mediendatei ist eine beliebige Mediendatei, der Regeln für die Verwendung des Inhalts zugeordnet sind. In einigen Fällen wird eine geschützte Mediendatei in Form der Digital Rights Management Verschlüsselung (DRM) verschlüsselt. Zum Wiedergeben einer geschützten Mediendatei muss die Wiedergabe im geschützten Medien Pfad (PMP) erfolgen. Außerdem muss der Benutzer möglicherweise Rechte für den Inhalt erhalten.

Der Begriff "Rechte Erfassung" bezieht sich auf jede Aktion, die die Anwendung ausführen muss, bevor der Benutzer den Inhalt wiedergeben kann. Das häufigste Beispiel ist das Abrufen einer DRM-Lizenz, Media Foundation jedoch einen generischen Mechanismus definiert, der andere Arten der Rechte Übernahme unterstützen kann. Die [**IMF contentenabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) -Schnittstelle definiert diesen generischen Mechanismus.

Die Rechte Übernahme muss außerhalb des PMP aus dem Anwendungsprozess erfolgen. Die Medien Sitzung benachrichtigt die Anwendung über die [**IMF contentprotection Manager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) -Schnittstelle, die von der Anwendung implementiert wird. Die Medien Sitzung verwendet die **imfcontentschutzmanager** -Schnittstelle zum Weiterleiten eines inhaltsenabler-Objekts an die Anwendung. Inhalts Enabler implementieren die [**IMF contentenabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) -Schnittstelle. Diese Schnittstelle wird von der Anwendung verwendet, um die erforderlichen Rechte zu erhalten.

Ein inhaltsenabler unterstützt möglicherweise die automatische Rechte Erfassung. in diesem Fall implementiert der Inhalts-Wegbereiter den gesamten Prozess, und die Anwendung überwacht einfach den Status. Andernfalls muss die Anwendung eine nicht automatische Rechte Übernahme verwenden. dabei handelt es sich um einen Prozess, bei dem die Anwendung HTTP Post-Daten an eine vom Inhalts-Enabler bereitgestellte URL sendet.

Zum Wiedergeben geschützter Medien befolgt eine Anwendung die gleichen Schritte wie im Thema [Abspielen von Mediendateien mit Media Foundation](how-to-play-unprotected-media-files.md)mit den folgenden zusätzlichen Schritten:

1.  Fragen Sie ab, ob die Medienquelle geschützte Inhalte enthält. (Optional.)
2.  Erstellen Sie die Medien Sitzung im PMP-Prozess anstelle des Anwendungsprozesses.
3.  Durchführen der Rechte Übernahme, wenn dies von der Medien Sitzung benachrichtigt wird. Dieser Vorgang wird asynchron von der Anwendung ausgeführt.
4.  Schließen Sie den asynchronen Vorgang ab.

## <a name="query-for-protected-content"></a>Abfragen geschützter Inhalte

Um abzufragen, ob eine Medienquelle geschützte Inhalte enthält, nennen Sie die [**mfrequireprotectedenvironment**](/windows/desktop/api/mfidl/nf-mfidl-mfrequireprotectedenvironment) -Funktion im Präsentations Deskriptor der Medienquelle. Wenn die Funktion S OK zurückgibt \_ , müssen Sie den Inhalt mit dem PMP wiedergeben. Wenn die Funktion S false zurückgibt \_ , ist das PMP nicht erforderlich, und Sie können die Medien Sitzung im Anwendungsprozess erstellen. Alternativ können Sie das PMP verwenden, um beide Arten von Inhalten, geschützt und ungeschützt, wiederzugeben. Wenn Sie dies tun, müssen Sie " **mfrequireprotectedenvironment**" nicht aufrufen.

Weitere Informationen zu Präsentations Deskriptoren finden Sie unter [Präsentations Deskriptoren](presentation-descriptors.md).

## <a name="create-the-pmp-media-session"></a>Erstellen der PMP-Medien Sitzung

Um die Medien Sitzung im PMP zu erstellen, rufen Sie [**mfkreatepmpmediasession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession)auf. Diese Funktion ähnelt [**mfkreatemediasession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession), aber statt die Medien Sitzung im Prozess der Anwendung zu erstellen, wird die Medien Sitzung im PMP-Prozess erstellt. Die Anwendung empfängt einen Zeiger auf ein Proxy Objekt für die Medien Sitzung. Die Anwendung ruft [**imfmediasession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) -Methoden für das Proxy Objekt auf, ebenso wie in der Medien Sitzung. Das Proxy Objekt leitet die Aufrufe an die Medien Sitzung über die Prozess Grenze weiter.

Erstellen Sie die PMP-Medien Sitzung wie folgt:

1.  Erstellen Sie einen neuen Attribut Speicher, indem Sie [**mfcreateattribute**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes)aufrufen.
2.  Legen Sie das Attribut " [**MF \_ Session \_ Content \_ Protection \_ Manager**](mf-session-content-protection-manager-attribute.md) " für den Attribut Speicher fest. Der Wert dieses Attributs ist ein Zeiger auf die Implementierung von [**imfcontentprotection Manager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager)Ihrer Anwendung. Der Befehl [**imfattributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown) wird aufgerufen, um das Attribut festzulegen.
3.  Rufen Sie [**mfkreatepmpmediasession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) auf, um die Medien Sitzung im PMP-Prozess zu erstellen. Der *pconfiguration* -Parameter ist ein Zeiger auf die [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstelle des Attribut Speicher.


```C++
IMFAttributes *pAttributes = NULL;
IMFMediaSession *pSession = NULL;

// Create the attribute store.
hr = MFCreateAttributes(&pAttributes, 1);

// Set the IMFContentProtectionManager pointer.
if (SUCCEEDED(hr))
{
    hr = pAttributes->SetUnknown(
        MF_SESSION_CONTENT_PROTECTION_MANAGER, 
        pCPM  // Your implementation of IMFContentProtectionManager.
        );
}

// Create the Media Session.
if (SUCCEEDED(hr))
{
    hr = MFCreatePMPMediaSession(
        0,
        pAttributes, 
        &pSession,
        NULL
    );
}

SAFE_RELEASE(pAttributes); // Release the attribute store.
// Use the Media Session to control playback (not shown).
```



Erstellen Sie als nächstes eine Wiedergabe Topologie, und stellen Sie Sie in der Medien Sitzung in eine Warteschlange, wie unter [Erstellen von Wiedergabe Topologien](creating-playback-topologies.md)beschrieben.

## <a name="perform-rights-acquisition"></a>Durchführen der Rechte Erfassung

Wenn die Wiedergabe eine Rechte Übernahme erfordert, ruft die Medien Sitzung [**IMF contentschutzmanager:: beginenablecontent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent)auf. Der Parameter " *pableraktivierungs* " dieser Methode ist ein Zeiger auf die [**imfactivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Schnittstelle. Verwenden Sie diese Schnittstelle zum Erstellen des Content Wegbereiter-Objekts, das die [**imfcontentenabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) -Schnittstelle verfügbar macht. Verwenden Sie dann den Inhalts-Wegbereiter, um den Schritt für die Rechte Übernahme auszuführen.

Rufen Sie zum Erstellen des Inhalts Enablers [**imfaktivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject)auf:


```C++
IMFContentEnabler *pEnabler = NULL;
hr = pEnablerActivate->ActivateObject(
    IID_IMFContentEnabler, 
    (void**)&pEnabler
    );
```



Fragen Sie den zurückgegebenen [**IMF contentenabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) -Zeiger für die [**IMF mediaeventgenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) -Schnittstelle ab. Verwenden Sie diese Schnittstelle, um Ereignisse aus dem Content Wegbereiter-Objekt zu erhalten. Weitere Informationen zu Ereignissen finden Sie unter [Medienereignis Generatoren](media-event-generators.md).

Um herauszufinden, ob der Inhalts Wegbereiter die automatische Erfassung unterstützt, nennen Sie [**imfcontentenabler:: isautomaticsupported**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-isautomaticsupported). Wenn diese Methode den Wert **true** zurückgibt, sollte die Anwendung die automatische Erfassung verwenden. Andernfalls verwenden Sie den nicht automatischen Erwerb.

Die [**beginenablecontent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) -Methode ist asynchron. Die Anwendung sollte den Erwerbs Schritt für den Thread der Anwendung ausführen. Ein Ansatz besteht darin, eine private Fenster Meldung an das Hauptfenster der Anwendung zu senden und den Anwendungs Thread zur Durchführung des Erwerbs zu benachrichtigen. Während der Vorgang ausstehend ist, muss die Anwendung den Rückruf Zeiger und das Zustands Objekt speichern, das in den Parametern *pCallback* und *punkstate* von **beginenablecontent** empfangen wurde. Diese werden verwendet, um den asynchronen Vorgang abzuschließen.

### <a name="automatic-acquisition"></a>Automatischer Erwerb

Um die automatische Erfassung durchzuführen, nennen Sie [**imfcontentenabler:: automaticenable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable). Diese Methode ist asynchron. Wenn der Vorgang abgeschlossen ist, sendet der Inhalts-Wegbereiter ein [meenablerabgeschlossene](meenablercompleted.md) -Ereignis. Der Statuscode des Ereignisses gibt an, ob der Vorgang erfolgreich war. Wenn der Statuscode des meenablerabgeschlossene-Ereignisses NS \_ E \_ DRM- \_ Lizenz \_ notbezogen ist, sollte die Anwendung versuchen, den nicht automatischen Erwerb zu verwenden.

Während der Übernahme Vorgang kann das Wegbereiter-Objekt das [meenablerprogress](meenablerprogress.md) -Ereignis senden, um den Fortschritt des Vorgangs anzuzeigen. Rufen Sie [**imfcontentenabler:: Cancel**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-cancel)auf, um den Vorgang abzubrechen.

### <a name="non-silent-acquisition"></a>Nicht automatische Beschaffung

Wenn die [**isautomaticsupported**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-isautomaticsupported) -Methode **false** zurückgibt oder die [**automaticenable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable) -Methode mit dem Fehlercode NS \_ E \_ DRM- \_ Lizenz notbezogen fehlschlägt \_ , sollte die Anwendung einen nicht automatischen Erwerb durchführen, wie in den folgenden Schritten beschrieben:

1.  Wenn Sie [**imfcontentenabler:: getenableurl**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-getenableurl) aufrufen, erhalten Sie die URL für den Erwerb der Rechte. Diese Methode gibt auch ein Flag zurück, das angibt, ob die URL vertrauenswürdig ist.
2.  Aufrufen von [**imfcontentenabler:: getenabledata**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-getenabledata) zum Abrufen der HTTP Post-Daten.
3.  Nennen Sie [**imfcontentenabler:: monitorenable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable). Diese Methode bewirkt, dass der Inhalts-Wegbereiter den Fortschritt der Rechte Erwerbs Aktion überwacht.

4.  Übermitteln Sie die Daten mithilfe einer HTTP Post-Aktion an die URL für die Rechte Erfassung. Sie können das Internet Explorer-Steuerelement oder die Windows Internet-APIs (WinInet) verwenden.

Der folgende Code zeigt die Schritte 1 – 3. Schritt 4 hängt von den speziellen Anforderungen Ihrer Anwendung ab.


```C++
WCHAR   *sURL = NULL;  // URL.
DWORD   cchURL = 0;    // Size of the URL in characters.

// Trust status of the URL.
MF_URL_TRUST_STATUS  trustStatus = MF_LICENSE_URL_UNTRUSTED;

BYTE    *pPostData = NULL;  // Buffer to hold HTTP POST data.
DWORD   cbPostDataSize = 0; // Size of the buffer, in bytes.

HRESULT hr = S_OK;

// Get the URL. 
hr = m_pEnabler->GetEnableURL(&sURL, &cchURL, &trustStatus);

if (SUCCEEDED(hr))
{
    if (trustStatus != MF_LICENSE_URL_TRUSTED)
    {
        // The URL is not trusted. Do not proceed.
        hr = E_FAIL;
    }
}

// Monitor the rights acquisition. 
if (SUCCEEDED(hr))
{
    hr = m_pEnabler->MonitorEnable();
}

// Get the HTTP POST data.
if (SUCCEEDED(hr))
{
    hr = m_pEnabler->GetEnableData(&pPostData, &cbPostDataSize);
}

// Open the URL and send the HTTP POST data. (Not shown.)

// Release the buffers.
CoTaskMemFree(pPostData);
CoTaskMemFree(sURL);
```



Wenn der Vorgang abgeschlossen ist, sendet der Inhalts-Wegbereiter ein [meenablerabgeschlossene](meenablercompleted.md) -Ereignis.

## <a name="complete-the-asynchronous-operation"></a>Asynchronen Vorgang beenden

Wenn die Rechte Erfassung erfolgreich oder anderweitig abgeschlossen ist, muss die Anwendung die Medien Sitzung Benachrichtigen, indem Sie den Rückruf Zeiger aufruft, der in der [**beginenablecontent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) -Methode angegeben ist.

1.  Erstellen Sie ein asynchrones Ergebnis Objekt, indem Sie [**mfcreateasyncresult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult)aufrufen.
2.  Rufen Sie den Rückruf der Medien Sitzung auf, indem Sie [**mfinvokecallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback)aufrufen.
3.  In der Medien Sitzung wird [**imfcontentschutzmanager:: erdenablecontent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-endenablecontent)aufgerufen. Geben Sie in ihrer Implementierung dieser Methode alle in [**beginenablecontent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent)zugeordneten Zeiger oder Ressourcen frei. Gibt ein **HRESULT** zurück, das den Gesamterfolg des Vorgangs angibt. Wenn die Rechte Beschaffung fehlgeschlagen ist oder der Benutzer vor dem Abschluss abgebrochen wurde, wird ein Fehlercode zurückgegeben.

Der folgende Code zeigt, wie das asynchrone Ergebnis erstellt und der Rückruf aufgerufen wird.


```C++
IMFAsyncResult  *pResult = NULL;

// Create the asynchronous result object.
hr = MFCreateAsyncResult(NULL, pCallback, punkState, &pResult);

// Invoke the callback.
if (SUCCEEDED(hr))
{
    pResult->SetStatus(hrStatus);
    hr = MFInvokeCallback(pResult);
}
SAFE_RELEASE(pResult);
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Medien Sitzung](media-session.md)
</dt> <dt>

[Audio-/Videowiedergabe](audio-video-playback.md)
</dt> </dl>

 

 



