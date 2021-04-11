---
description: Legt einen Rückruf fest, der während der Quell Auflösung die PMP-Medien Sitzung erstellt.
ms.assetid: 7277C5E0-BB91-4EEA-9529-64E66D179CDC
title: MFPKEY_PMP_Creation_Callback-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2b18e04a15e035a9e4dc04a4039ce230342031a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215502"
---
# <a name="mfpkey_pmp_creation_callback-property"></a>Rückruf Eigenschaft für mfpkey \_ PMP- \_ Erstellung \_

Legt einen Rückruf fest, der während der Quell Auflösung die [PMP-Medien Sitzung](pmp-media-session.md) erstellt.



Datentyp

PROPVARIANT-Typ (VT)

PROPVARIANT-Member

**IUnknown \** _

VT \_ unbekannt

_ *punkVal**



## <a name="remarks"></a>Bemerkungen

Für einige geschützte Inhalte ist möglicherweise die Verwendung dieser Eigenschaft erforderlich. Wenn dies der Fall ist, tritt bei der Quell Auflösung ein Fehler auf, und der Fehlercode **MF \_ E \_ \_ erfordert \_ PMP- \_ Erstellungs \_ Rückruf**.

Gehen Sie folgendermaßen vor, um diese Eigenschaft zu verwenden.

1.  Rufen Sie [**pscreatememorypropertystore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) auf, um einen Eigenschafts Speicher zu erstellen.
2.  Implementieren Sie die [**imfasynccallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) -Rückruf Schnittstelle.
3.  Legen Sie die \_ Eigenschaft Rückruf für mfpkey PMP- \_ Erstellung \_ für den Eigenschaften Speicher fest. Der Wert ist ein Zeiger auf die [**imfasynccallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) -Implementierung.
4.  Aufrufen von [**imfsourceresolver:: beginkreateobjectfromurl**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl). Übergeben Sie einen Zeiger auf den Eigenschaften Speicher im *prequiterparameter* .

Führen Sie in der [**imfasynccallback:: Aufrufen**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) -Methode Ihrer Rückruf Schnittstelle die folgenden Schritte aus.

1.  Rufen Sie [**mfkreatepmpmediasession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) auf, um die [PMP-Medien Sitzung](pmp-media-session.md)zu erstellen.
2.  Aufrufen von [**imfgetservice:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) in der PMP-Medien Sitzung an einen Zeiger auf die [**imfpmphost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) -Schnittstelle.
3.  Rufen Sie [**imfasynkresult:: GetState**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate) für das Result-Objekt auf, das im *pasynkresult* -Parameter von [**imfasynccallback:: Aufrufen**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke)übergeben wird. Fragen Sie den zurückgegebenen [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Zeiger für die [**imfasynccallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) -Schnittstelle ab.
4.  Nennen Sie [**mfputworkitem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) mit den folgenden Parametern:
    -   *dwqueue*: **mfasync- \_ Rückruf \_ Warteschlangen \_ Standard**
    -   *pCallback*: der [**imfasynccallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) -Zeiger, der in Schritt 3 abgerufen wurde.
    -   *pState*: der [**imfpmphost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) -Zeiger, der in Schritt 2 abgerufen wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8 \[ -Desktop-Apps \| UWP-apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> <dt>

[PMP-Medien Sitzung](pmp-media-session.md)
</dt> <dt>

[Geschützter Medien Pfad](protected-media-path.md)
</dt> <dt>

[Quellresolver](source-resolver.md)
</dt> </dl>

 

 
