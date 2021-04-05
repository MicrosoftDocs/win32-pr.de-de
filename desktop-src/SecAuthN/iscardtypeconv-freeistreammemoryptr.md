---
description: Gibt den Byte Zeiger frei, der auf den von einer IStream-com-Schnittstelle verwalteten HGLOBAL-Speicherblock zeigt.
ms.assetid: a76c97a9-d0e9-4eb0-9f97-15f22111187d
title: 'Iscardtypekonv:: freeistreammemoryptr-Methode (scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.FreeIStreamMemoryPtr
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 12912b8130ed6e1ccaa995f88069b59e96f57c09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103756876"
---
# <a name="iscardtypeconvfreeistreammemoryptr-method"></a>Iscardtypekonv:: freeistreammemoryptr-Methode

\[Die **freeistreammemoryptr** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die **freeistreammemoryptr** -Methode gibt den Byte Zeiger frei, der auf den von einer **IStream** -com-Schnittstelle verwalteten HGLOBAL-Speicherblock zeigt.

## <a name="syntax"></a>Syntax


```C++
HRESULT FreeIStreamMemoryPtr(
  [in] LPSTREAM pStrm,
  [in] LPBYTE   pMem
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pstraum* \[ in\]
</dt> <dd>

Ein Zeiger auf die **IStream** -Schnittstelle, die den Speicherblock verwaltet, auf den *pMem* zeigt.

</dd> <dt>

*pMem* \[ in\]
</dt> <dd>

Zeiger auf den von der **IStream** -Schnittstelle verwalteten Speicherblock.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt einen der folgenden möglichen Werte zurück:



| Rückgabecode                                                                                   | Beschreibung                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Der Arbeitsspeicher wurde erfolgreich zugewiesen.<br/>                                                        |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Bei einem oder mehreren Parametern, die an die Funktion weitergegeben wurden, ist ein Fehler aufgetreten.<br/> |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Ein Parameter vom Zeigertyp war falsch.<br/>                                            |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Nicht genügend freier Arbeitsspeicher, um die Anforderung zu erfüllen.<br/>                                            |



 

## <a name="remarks"></a>Bemerkungen

Diese Funktion gibt vollständig und sauber den Byte Zeiger frei, der auf den von der **IStream** -Schnittstelle verwalteten HGLOBAL-Speicherblock zeigt. Der Byte Zeiger wird durch einen get-Befehl von [**getatistreammemory**](iscardtypeconv-getatistreammemory.md)abgerufen.

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
</dt> <dt>

[**Getatistreammemory**](iscardtypeconv-getatistreammemory.md)
</dt> </dl>

 

 
