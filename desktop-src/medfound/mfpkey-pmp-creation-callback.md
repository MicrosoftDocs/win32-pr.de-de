---
description: Legt einen Rückruf fest, der die PMP-Mediensitzung während der Quellauflösung erstellt.
ms.assetid: 7277C5E0-BB91-4EEA-9529-64E66D179CDC
title: MFPKEY_PMP_Creation_Callback -Eigenschaft (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 655d61865eaecd89fa84664fc5c25f89762180ac9007e21cc7cbc98f7a68b056
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953860"
---
# <a name="mfpkey_pmp_creation_callback-property"></a>MFPKEY \_ PMP \_ Creation \_ Callback-Eigenschaft

Legt einen Rückruf fest, der die [PMP-Mediensitzung während](pmp-media-session.md) der Quellauflösung erstellt.



Datentyp

PROPVARIANT-Typ (vt)

PROPVARIANT-Member

**IUnknown\***

VT \_ UNKNOWN

**beival**



## <a name="remarks"></a>Hinweise

Einige geschützte Inhalte erfordern möglicherweise die Verwendung dieser Eigenschaft. Wenn dies der Wert ist, schlägt der Quellauflösungsprozess mit dem Fehlercode **MF \_ E RESOLUTION REQUIRES \_ \_ \_ PMP CREATION \_ \_ CALLBACK fehl.**

Gehen Sie wie folgt vor, um diese Eigenschaft zu verwenden.

1.  Rufen [**Sie PSCreateMemoryPropertyStore auf,**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) um einen Eigenschaftenspeicher zu erstellen.
2.  Implementieren Sie [**die RÜCKRUF-Schnittstelle FÜR DIE Asynchrone**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) Rückrufe.
3.  Legen Sie die MFPKEY \_ PMP \_ Creation \_ Callback-Eigenschaft für den Eigenschaftenspeicher fest. Der Wert ist ein Zeiger auf die [**IMPLEMENTIERUNG VONASYNCCallback.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback)
4.  Rufen [**Sie DANNSOURCEResolver::BeginCreateObjectFromURL auf.**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) Übergeben Sie einen Zeiger auf den Eigenschaftenspeicher im *pProps-Parameter.*

Führen Sie [**in der METHODEASYNCCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) Ihrer Rückrufschnittstelle Folgendes aus.

1.  Rufen [**Sie MFCreatePMPMediaSession auf,**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) um die [PMP-Mediensitzung zu erstellen.](pmp-media-session.md)
2.  Rufen [**Sie INGEGETService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) in der PMP-Mediensitzung auf einen Zeiger auf die [**IMFPMPHost-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) auf.
3.  Rufen [**Sie FÜR DAS ERGEBNISOBJEKT::GetState**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate) auf, das im *pAsyncResult-Parameter* [**vonASYNCCallback::Invoke übergeben wird.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) Fragen Sie den [**zurückgegebenen IUnknown-Zeiger**](/windows/win32/api/unknwn/nn-unknwn-iunknown) für [**dieASYNCCallback-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) ab.
4.  Rufen [**Sie MFPutWorkItem mit**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) den folgenden Parametern auf:
    -   *dwQueue:* **MFASYNC \_ CALLBACK \_ QUEUE \_ STANDARD**
    -   *pCallback:* Der IN Schritt 3 [**erhalteneASYNCCallback-Zeiger.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback)
    -   *pState:* Der im Schritt 2 erhaltene [**IMFPMPHost-Zeiger.**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Desktop-Apps \| UWP-Apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Desktop-Apps \| UWP-Apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Eigenschaften](media-foundation-properties.md)
</dt> <dt>

[PMP-Mediensitzung](pmp-media-session.md)
</dt> <dt>

[Geschützter Medienpfad](protected-media-path.md)
</dt> <dt>

[Quellre resolver](source-resolver.md)
</dt> </dl>

 

 
