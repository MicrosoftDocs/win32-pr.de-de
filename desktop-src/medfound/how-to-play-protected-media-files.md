---
description: Hier erfahren Sie, wie Sie Dateien wiederverspielen, die DRM-geschützte Medien enthalten.
ms.assetid: 85d98f49-8af2-42ce-9b36-a025aee93f73
title: Wiederspielen geschützter Mediendateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c20a2b525f8acc3a602bcaae2630726d01269881beec07ac214f4d0bd02ee1cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942340"
---
# <a name="how-to-play-protected-media-files"></a>Wiederspielen geschützter Mediendateien

Eine geschützte Mediendatei ist jede Mediendatei, der Regeln für die Verwendung des Inhalts zugeordnet sind. In einigen Fällen wird eine geschützte Mediendatei mit einer Form der DRM-Verschlüsselung (Digital Rights Management) verschlüsselt. Um eine geschützte Mediendatei wiedergeben zu können, muss die Wiedergabe innerhalb des geschützten Medienpfads (PMP) erfolgen. Darüber hinaus muss der Benutzer möglicherweise Rechte für den Inhalt erwerben.

Der Begriff Rechteerwerb bezieht sich auf jede Aktion, die die Anwendung ausführen muss, bevor der Benutzer den Inhalt wieder spielen kann. Das häufigste Beispiel ist das Abrufen einer DRM-Lizenz, aber Media Foundation definiert einen generischen Mechanismus, der andere Arten von Rechteerwerb unterstützen kann. Diese generischen Mechanismen werden von der [**BENUTZEROBERFLÄCHEContentEnabler-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) definiert.

Der Rechteerwerb muss außerhalb des PMP über den Anwendungsprozess erfolgen. Die Mediensitzung benachrichtigt die Anwendung über die VON der Anwendung [**implementierte BENUTZEROBERFLÄCHEContentProtectionManager-Schnittstelle.**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) Die Mediensitzung verwendet die **BENUTZEROBERFLÄCHEContentProtectionManager-Schnittstelle,** um ein Inhalts-Enabler-Objekt an die Anwendung weiter zu geben. Inhalts-Enabler implementieren die [**BENUTZEROBERFLÄCHEContentEnabler-Schnittstelle.**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) Die Anwendung verwendet diese Schnittstelle, um die erforderlichen Rechte zu erhalten.

Eine Inhaltsaktivierung unterstützt möglicherweise den automatischen Rechteerwerb. In diesem Fall implementiert die Inhaltsaktivierung den gesamten Prozess, und die Anwendung überwacht einfach den Status. Andernfalls muss die Anwendung den nicht automatischen Rechteerwerb verwenden. Dies ist ein Prozess, bei dem die Anwendung HTTP POST-Daten an eine URL sendet, die vom Inhaltsaktivierer bereitgestellt wird.

Um geschützte Medien wieder zu verwenden, folgt eine Anwendung den im Thema How [to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md)beschriebenen Schritten mit den folgenden zusätzlichen Schritten:

1.  Fragen Sie ab, ob die Medienquelle geschützten Inhalt enthält. (Optional.)
2.  Erstellen Sie die Mediensitzung im PMP-Prozess anstelle des Anwendungsprozesses.
3.  Führen Sie den Rechteerwerb aus, wenn Sie von der Mediensitzung dazu benachrichtigt werden. Dieser Vorgang wird asynchron von der Anwendung ausgeführt.
4.  Schließen Sie den asynchronen Vorgang ab.

## <a name="query-for-protected-content"></a>Abfragen von geschütztem Inhalt

Um zu abfragen, ob eine Medienquelle geschützten Inhalt enthält, rufen Sie die [**MFRequireProtectedEnvironment-Funktion**](/windows/desktop/api/mfidl/nf-mfidl-mfrequireprotectedenvironment) für den Präsentationsdeskriptor der Medienquelle auf. Wenn die Funktion S \_ OK zurückgibt, müssen Sie den Inhalt mithilfe von PMP wiedergibt. Wenn die Funktion S FALSE zurückgibt, ist der PMP nicht erforderlich, und Sie können die \_ Mediensitzung im Anwendungsprozess erstellen. Alternativ können Sie den PMP verwenden, um beide Inhaltstypen (geschützt und ungeschützte Inhalte) wieder anzuzeigen. Wenn Sie dies tun, müssen Sie **MFRequireProtectedEnvironment nicht aufrufen.**

Weitere Informationen zu Präsentationsdeskriptoren finden Sie unter [Präsentationsdeskriptoren.](presentation-descriptors.md)

## <a name="create-the-pmp-media-session"></a>Erstellen der PMP-Mediensitzung

Um die Mediensitzung im PMP zu erstellen, rufen Sie [**MFCreatePMPMediaSession auf.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) Diese Funktion ähnelt [**MFCreateMediaSession,**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession)aber anstatt die Mediensitzung im Prozess der Anwendung zu erstellen, wird die Mediensitzung im PMP-Prozess erstellt. Die Anwendung empfängt einen Zeiger auf ein Proxyobjekt für die Mediensitzung. Die Anwendung ruft WIE in der Mediensitzung [**DIE METHODEN FÜR DIEMEDIASESSION**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) für das Proxyobjekt auf. Das Proxyobjekt gibt die Aufrufe an die Mediensitzung über die Prozessgrenze hinaus weiter.

Erstellen Sie die PMP-Mediensitzung wie folgt:

1.  Erstellen Sie einen neuen Attributspeicher, indem [**Sie MFCreateAttributes aufrufen.**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes)
2.  Legen Sie das [**MF \_ SESSION CONTENT \_ PROTECTION \_ \_ MANAGER-Attribut**](mf-session-content-protection-manager-attribute.md) für den Attributspeicher fest. Der Wert dieses Attributs ist ein Zeiger auf die Implementierung von [**DURCHZEIGERContentProtectionManager in Ihrer Anwendung.**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) Rufen [**Sie DIE ATTRIBUTE::SetUnknown auf,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown) um das Attribut zu festlegen.
3.  Rufen [**Sie MFCreatePMPMediaSession auf,**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) um die Mediensitzung im PMP-Prozess zu erstellen. Der *pConfiguration-Parameter* ist ein Zeiger auf die [**ATTRIBUTEAttributes-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) des Attributspeichers.


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



Erstellen Sie als Nächstes eine Wiedergabetopologie, und stellen Sie sie in der Mediensitzung in die Warteschlange ein, wie unter [Erstellen von Wiedergabetopologien beschrieben.](creating-playback-topologies.md)

## <a name="perform-rights-acquisition"></a>Ausführen des Rechteerwerbs

Wenn für die Wiedergabe ein Rechteerwerb erforderlich ist, ruft die Mediensitzung [**DENTContentProtectionManager::BeginEnableContent auf.**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) Der *pEnablerActivate-Parameter* dieser Methode ist ein Zeiger auf die [**BERActivate-Schnittstelle.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) Verwenden Sie diese Schnittstelle, um das Content Enabler-Objekt zu erstellen, das die [**BENUTZEROBERFLÄCHEContentEnabler-Schnittstelle verfügbar**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) macht. Verwenden Sie dann den Inhaltsaktivierer, um den Schritt zum Erwerb von Rechten durchzuführen.

Um die Inhaltsaktivierung zu erstellen, rufen [**Sie DIEACTIVate::ActivateObject auf:**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject)


```C++
IMFContentEnabler *pEnabler = NULL;
hr = pEnablerActivate->ActivateObject(
    IID_IMFContentEnabler, 
    (void**)&pEnabler
    );
```



Fragen Sie den [**zurückgegebenen POINTERCONTENTEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) für die [**BERMEDIAEventGenerator-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) ab. Verwenden Sie diese Schnittstelle, um Ereignisse aus dem Content Enabler-Objekt zu erhalten. Weitere Informationen zu Ereignissen finden Sie unter [Media Event Generators](media-event-generators.md).

Um herauszufinden, ob die Inhaltsermöglichung den automatischen Abruf unterstützt, rufen [**Sie DENTContentEnabler::IsAutomaticSupported auf.**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-isautomaticsupported) Wenn diese Methode den Wert **TRUE zurückgibt,** sollte die Anwendung den automatischen Erwerb verwenden. Verwenden Sie andernfalls den nicht automatischen Erwerb.

Die [**BeginEnableContent-Methode**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) ist asynchron. Die Anwendung sollte den Übernahmeschritt im Thread der Anwendung ausführen. Ein Ansatz besteht in der Benachrichtigung eines privaten Fensters im Hauptfenster der Anwendung, den Anwendungsthread über die Durchführung des Kaufs zu benachrichtigen. Während der Vorgang aussteht, muss die Anwendung den Rückrufzeiger und das Zustandsobjekt speichern, das sie in den *Parametern pCallback* und *statusState* von **BeginEnableContent empfangen hat.** Diese werden zum Abschließen des asynchronen Vorgangs verwendet.

### <a name="automatic-acquisition"></a>Automatische Übernahme

Um den automatischen Abruf durchzuführen, rufen [**Sie DENTContentEnabler::AutomaticEnable auf.**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable) Diese Methode ist asynchron. Wenn der Vorgang abgeschlossen ist, sendet die Inhaltsermöglichung ein [MEEnablerCompleted-Ereignis.](meenablercompleted.md) Der Statuscode des Ereignisses gibt an, ob der Vorgang erfolgreich war. Wenn der Statuscode des MEEnablerCompleted-Ereignisses NS \_ E \_ DRM \_ LICENSE NOTACQUIRED ist, sollte die Anwendung versuchen, den nicht automatischen Erwerb \_ zu verwenden.

Während der Beschaffungsvorgang wird durchgeführt, sendet das Enabler-Objekt möglicherweise das [MEEnablerProgress-Ereignis,](meenablerprogress.md) um den Fortschritt des Vorgangs anzugeben. Um den Vorgang abzubruchen, rufen [**Sie DENTContentEnabler::Cancel auf.**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-cancel)

### <a name="non-silent-acquisition"></a>Nicht automatischer Erwerb

Wenn die [**IsAutomaticSupported-Methode**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-isautomaticsupported) **FALSE** zurückgibt oder die [**AutomaticEnable-Methode**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable) mit dem Fehlercode NS \_ E \_ DRM \_ LICENSE NOTACQUIRED fehlschlägt, sollte die Anwendung einen nicht automatischen Erwerb durchführen, wie in den folgenden Schritten \_ beschrieben:

1.  Rufen Sie ZUM Abruf der URL für den Rechteerwerb [**DIE URL ZU BERCONTENTEnabler::GetEnableURL**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-getenableurl) auf. Diese Methode gibt auch ein Flag zurück, das angibt, ob die URL vertrauenswürdig ist.
2.  Rufen Sie ZUM Abruf der HTTP [**POST-Daten DEN WERTCONTENTEnabler::GetEnableData**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-getenabledata) auf.
3.  Rufen [**Sie DEN AUFRUF VON ZUECONTENTEnabler::MonitorEnable auf.**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable) Diese Methode bewirkt, dass der Inhaltsaktivierer den Fortschritt der Rechteerwerbsaktion überwacht.

4.  Übermitteln Sie die Daten mithilfe einer HTTP POST-Aktion an die Rechteerwerbs-URL. Sie können das Internet Explorer-Steuerelement oder die Windows Internet-APIs (WinINet) verwenden.

Der folgende Code zeigt die Schritte 1 bis 3. Schritt 4 hängt von den speziellen Anforderungen Ihrer Anwendung ab.


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



Wenn der Vorgang abgeschlossen ist, sendet die Inhaltsermöglichung ein [MEEnablerCompleted-Ereignis.](meenablercompleted.md)

## <a name="complete-the-asynchronous-operation"></a>Abschließen des asynchronen Vorgangs

Nach erfolgreichem oder anderweitigen Abschluss des Rechteerwerbs muss die Anwendung die Mediensitzung benachrichtigen, indem sie den in der [**BeginEnableContent-Methode angegebenen Rückrufzeiger**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) aufruft.

1.  Erstellen Sie ein asynchrones Ergebnisobjekt, indem [**Sie MFCreateAsyncResult aufrufen.**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult)
2.  Rufen Sie den Rückruf der Mediensitzung auf, indem [**Sie MFInvokeCallback aufrufen.**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback)
3.  Die Mediensitzung aufruft [**DENTContentProtectionManager::EndEnableContent.**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-endenablecontent) Geben Sie in Ihrer Implementierung dieser Methode alle Zeiger oder Ressourcen frei, die Sie in [**BeginEnableContent zugeordnet haben.**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) Gibt ein **HRESULT zurück,** das den Gesamterfolg des Vorgangs angibt. Wenn der Rechteerwerb fehlgeschlagen ist oder der Benutzer abgebrochen wurde, bevor er abgeschlossen wurde, geben Sie einen Fehlercode zurück.

Der folgende Code zeigt, wie sie das asynchrone Ergebnis erstellen und den Rückruf aufrufen.


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

[Mediensitzung](media-session.md)
</dt> <dt>

[Audio-/Videowiedergabe](audio-video-playback.md)
</dt> </dl>

 

 



