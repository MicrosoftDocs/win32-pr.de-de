---
description: Ruft einen Byte Zeiger auf den hglobal-Speicherblock ab, der von der IStream-com-Schnittstelle verwaltet wird.
ms.assetid: ea25eb98-b841-4f5e-b428-3d9cb8176142
title: 'Iscardtypekonv:: getatistreammemory-Methode (scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.GetAtIStreamMemory
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: bdd828921f18c3d06edd2d41da189260a4ed4394
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750033"
---
# <a name="iscardtypeconvgetatistreammemory-method"></a>Iscardtypekonv:: getatistreammemory-Methode

\[Die **getatistreammemory** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die **getatistreammemory** -Methode erhält einen Byte Zeiger auf den hglobal-Speicherblock, der von der **IStream** -com-Schnittstelle verwaltet wird.

Dies ist eine Möglichkeit, um den Arbeitsspeicher unter dem **IStream** zu erhalten, ohne den sizeof-Wert für den Speicherblock in Bytes zu erhalten und die Bytes mithilfe der **IStream** -Schnittstelle in ein temporäres Bytearray zu lesen.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetAtIStreamMemory(
  [in]  LPSTREAM    pStrm,
  [out] LPBYTEARRAY *ppMem
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pstraum* \[ in\]
</dt> <dd>

Ein Zeiger auf die **IStream** -com-Schnittstelle, die den hglobal-Speicherblock verwaltet.

</dd> <dt>

*ppMem* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf das erste Byte des HGLOBAL-Speicherblocks, wenn der Vorgang erfolgreich war. andernfalls **null** , wenn der Vorgang fehlschlägt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                   | Beschreibung                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Der Arbeitsspeicher wurde erfolgreich zugewiesen.<br/>                                                        |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Bei einem oder mehreren Parametern, die an die Funktion weitergegeben wurden, ist ein Fehler aufgetreten.<br/> |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Ein Parameter vom Zeigertyp war falsch.<br/>                                            |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Nicht genügend freier Arbeitsspeicher, um die Anforderung zu erfüllen.<br/>                                            |



 

## <a name="remarks"></a>Bemerkungen

Der **IStream** -Verweis Zähler wird für jeden abgerufenen *ppMem* -Zeiger inkrementiert.

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

 

 
