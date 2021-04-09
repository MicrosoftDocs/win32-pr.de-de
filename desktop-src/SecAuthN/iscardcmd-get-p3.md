---
description: Ruft den dritten Parameter (P3) aus der Anwendungsprotokoll Dateneinheit (APDU) ab.
ms.assetid: 5fe90686-f542-42be-91ed-6600eaee3e7b
title: 'Iscardcmd:: get_P3-Methode (scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_P3
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: b1072fc9c4ca3b2a238cc8893104df1a831c99c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129340"
---
# <a name="iscardcmdget_p3-method"></a>Iscardcmd:: get \_ P3-Methode

\[Die **get \_ P3** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die **get \_ P3** -Methode ruft den dritten Parameter (P3) aus der [*Application Protocol Data Unit*](../secgloss/a-gly.md) (APDU) ab. Dieser schreibgeschützte Bytewert stellt die Größe des Datentyps des APDU dar.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_P3(
  [out] BYTE *pbyP3
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pbyP3* \[ vorgenommen\]
</dt> <dd>

Zeiger auf das Byte, das bei der Rückgabe aus dem APDU P3 ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                   | Beschreibung                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operation erfolgreich abgeschlossen.<br/>    |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Der *pbyP3* ist ungültig.<br/>            |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | In *pbyP3* wurde ein fehlerhafter Zeiger übermittelt.<br/> |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                       |



 

## <a name="remarks"></a>Bemerkungen

Der P3-Parameter ist schreibgeschützt und kann daher nicht festgelegt werden.

Zum Abrufen der Parameter "P1" oder "P2" müssen [**Sie get \_ P1**](iscardcmd-get-p1.md) bzw. [**\_ P2**](iscardcmd-get-p2.md) abrufen.

Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**iscardcmd**](iscardcmd.md).

Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die [*Smartcard*](../secgloss/s-gly.md) zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird gezeigt, wie das dritte Parameter-Byte (P3) aus der [*Anwendungsprotokoll Daten-Einheit (Application Protocol Data Unit*](../secgloss/a-gly.md) , APDU) abgerufen wird. Im Beispiel wird davon ausgegangen, dass "piscardcmd" ein gültiger Zeiger auf eine Instanz der [**iscardcmd**](iscardcmd.md) -Schnittstelle ist.


```C++
BYTE  byP3;
HRESULT  hr;

// Retrieve the P3 byte.
hr = pISCardCmd->get_P3(&byP3);
if (FAILED(hr))
{
  printf("Failed get_P3\n");
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

[**\_P1 erhalten**](iscardcmd-get-p1.md)
</dt> <dt>

[**\_P2 erhalten**](iscardcmd-get-p2.md)
</dt> <dt>

[**Iscardcmd**](iscardcmd.md)
</dt> </dl>

 

 
