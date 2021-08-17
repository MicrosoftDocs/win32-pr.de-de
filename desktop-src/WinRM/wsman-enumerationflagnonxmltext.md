---
title: WSMan.EnumerationFlagNonXmlText-Methode (WSManDisp.h)
description: Gibt den Wert der Enumerationskonstante WSManFlagNonXmlText für die Verwendung im flags-Parameter der Session.Enumerate-Methode zurück.
ms.assetid: 5e062e73-f833-4090-ba5a-48ca374724e7
ms.tgt_platform: multiple
keywords:
- EnumerationFlagNonXmlText-Methode Windows Remoteverwaltung
- EnumerationFlagNonXmlText-Methode Windows Remoteverwaltung, WSMan-Objekt
- WSMan-Objekt Windows Remoteverwaltung , EnumerationFlagNonXmlText-Methode
topic_type:
- apiref
api_name:
- WSMan.EnumerationFlagNonXmlText
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6606a20d0ab7f59b7521367243ccdc97fd90209f1791d8f1ded3e48c70e3f59
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742289"
---
# <a name="wsmanenumerationflagnonxmltext-method"></a>WSMan.EnumerationFlagNonXmlText-Methode

**WSMan.EnumerationFlagNonXmlText** gibt den Wert der **Enumerationskonstante WSManFlagNonXmlText** für die Verwendung im *flags-Parameter* der [**Session.Enumerate-Methode**](session-enumerate.md) zurück. Diese Methode bietet eine effizientere Syntax für die Verwendung der -Konstante, sodass skripts nicht erforderlich sind, um einen konstanten Wert festzulegen. Weitere Informationen zum Aufrufen dieser Methode finden Sie unter [Sitzungskonstanten.](session-constants.md)

**WSManFlagNonXmlText** ist eine Konstante in der **\_ \_ WSManEnumFlags-Enumeration.** Weitere Informationen finden Sie unter [**Enumerationskonstanten.**](enumeration-constants.md)

## <a name="syntax"></a>Syntax


```VB
WSMan.EnumerationFlagNonXmlText( _
  ByRef flags _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Flags* \[ out\]
</dt> <dd>

Der Wert der Konstante.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Header<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Wsman**](wsman.md)
</dt> <dt>

[**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex)
</dt> <dt>

[**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession)
</dt> </dl>

 

 





