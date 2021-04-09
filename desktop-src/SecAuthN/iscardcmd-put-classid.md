---
description: Legt einen neuen Klassen Bezeichner in der Application Protocol Data Unit (APDU) fest.
ms.assetid: 7e7d42f2-2858-4b37-a7d5-a919e3e005da
title: Iscardcmd::p ut_ClassId-Methode (scarddat. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_ClassId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ed4b1f273ebe9ea0a5e105ec3d88fc8446f7a831
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959172"
---
# <a name="iscardcmdput_classid-method"></a>Iscardcmd::p UT \_ ClassID-Methode

\[Die **Put \_ ClassID-** Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die **Put \_ ClassID-** Methode legt einen neuen Klassen Bezeichner in der [*Application Protocol Data Unit*](../secgloss/a-gly.md) (APDU) fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_ClassId(
  [in] BYTE byClass
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*byclass* \[ in\]
</dt> <dd>

Das Byte, das den Klassen Bezeichner darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                   | Beschreibung                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operation erfolgreich abgeschlossen.<br/> |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Die *byclass* ist ungültig.<br/>       |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                    |



 

## <a name="remarks"></a>Bemerkungen

Rufen Sie zum Abrufen des aktuellen Klassen Bezeichners [**get \_ ClassID**](iscardcmd-get-classid.md)auf.

Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**iscardcmd**](iscardcmd.md).

Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die [*Smartcard*](../secgloss/s-gly.md) zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt, wie Sie einen neuen Klassen Bezeichner in der [*Anwendungsprotokoll Daten-Einheit (Application Protocol Data Unit*](../secgloss/a-gly.md) , APDU) festlegen. Im Beispiel wird davon ausgegangen, dass "piscardcmd" ein gültiger Zeiger auf eine Instanz der [**iscardcmd**](iscardcmd.md) -Schnittstelle ist.


```C++
HRESULT  hr;

// Set the class ID.
hr = pISCardCmd->put_ClassId(0xC0);
if (FAILED(hr))
{
  printf("Failed put_ClassId\n");
  // Take other error handling action as needed.
}
```



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
| IID<br/>                      | IID \_ iscardcmd ist als D5778AE3-43DE-11D0-9171-00AA00C18068 definiert.<br/>            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_ClassID Get**](iscardcmd-get-classid.md)
</dt> <dt>

[**Iscardcmd**](iscardcmd.md)
</dt> </dl>

 

 
