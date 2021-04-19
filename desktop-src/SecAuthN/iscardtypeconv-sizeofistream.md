---
description: Bestimmt die Größe (in Bytes) der IStream-com-Schnittstelle.
ms.assetid: 8c2f081d-cc41-409e-a868-bcf834e1f128
title: 'Iscardtypekonv:: sizeofstream-Methode (scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.SizeOfIStream
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 603a01dc6cb4727d59a7fb82c3270c08a495f021
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359109"
---
# <a name="iscardtypeconvsizeofistream-method"></a>Iscardtypekonv:: sizeofstream-Methode

\[Die **sizeofstream** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die **sizeofstream** -Methode bestimmt die Größe der **IStream** -com-Schnittstelle in Byte.

## <a name="syntax"></a>Syntax


```C++
HRESULT SizeOfIStream(
  [in]  LPSTREAM       pStrm,
  [out] ULARGE_INTEGER *puliSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pstraum* \[ in\]
</dt> <dd>

Ein Zeiger auf die **IStream** -com-Schnittstelle.

</dd> <dt>

*pulisize* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf die große ganze Zahl ohne Vorzeichen, die den gesamten 64-Bit-sizeof-Wert der **IStream** -com-Schnittstelle enthalten kann.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                  | Beschreibung                                                                                             |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Die Funktion war erfolgreich, und " *\* pulisize* " ist die Größe (in Bytes) der IStream-com-Schnittstelle.<br/> |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl>       | Ein nicht spezifizierter Fehler ist aufgetreten.<br/>                                                                |
| <dl> <dt>**E \_ invalidArg**</dt> </dl> | Der " *pulisize* "-Parameter ist falsch.<br/>                                                       |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>    | Der *pstrinm* -Parameter ist falsch.<br/>                                                          |
| <dl> <dt>**E \_ unerwartet**</dt> </dl> | Unerwarteter Fehler.<br/>                                                                   |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                   |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>"Scarddat. h"</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Scarddat. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ iscardtypec ist als 53b6aa63-3F 56-11D0-916b-00aa00c18068 definiert.<br/>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iscardtypeconfiguration**](iscardtypeconv.md)
</dt> <dt>

[Smartcard-Rückgabewerte](authentication-return-values.md)
</dt> </dl>

 

 
