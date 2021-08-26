---
description: Ruft das dritte Parameter-Byte (P3) aus der Anwendungsprotokolldateneinheit (Application Protocol Data Unit, APDU) ab.
ms.assetid: 5fe90686-f542-42be-91ed-6600eaee3e7b
title: ISCardCmd::get_P3-Methode (Ddat.h)
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
ms.openlocfilehash: 4ebf19856126d65824b9214973aa90412475afeecf707a17f9b9434d9852945f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014920"
---
# <a name="iscardcmdget_p3-method"></a>ISCardCmd::get \_ P3-Methode

\[Die **\_ Get P3-Methode** ist für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **\_ get P3-Methode** ruft das dritte Parameter byte (P3) aus der [*Application Protocol Data Unit*](../secgloss/a-gly.md) (APDU) ab. Dieser schreibgeschützte Bytewert stellt die Größe des Datenteils der APDU dar.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_P3(
  [out] BYTE *pbyP3
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pbyP3* \[ out\]
</dt> <dd>

Zeiger auf das Byte, das bei der Rückgabe vom APDU P3 ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                   | Beschreibung                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operation erfolgreich abgeschlossen.<br/>    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | *PbyP3* ist ungültig.<br/>            |
| <dl> <dt>**E \_ POINTER**</dt> </dl>     | Ein ungültiger Zeiger wurde in *pbyP3* übergeben.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                       |



 

## <a name="remarks"></a>Hinweise

Der P3-Parameter ist schreibgeschützt und kann daher nicht festgelegt werden.

Um die P1- oder P2-Parameter abzurufen, rufen [**Sie \_ get P1**](iscardcmd-get-p1.md) bzw. [**\_ P2 auf.**](iscardcmd-get-p2.md)

Eine Liste aller von dieser Schnittstelle bereitgestellten Methoden finden Sie unter [**ISCardCmd**](iscardcmd.md).

Zusätzlich zu den oben aufgeführten COM-Fehlercodes kann diese Schnittstelle einen [*Smartcardfehlercode*](../secgloss/s-gly.md) zurückgeben, wenn eine Smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte.](authentication-return-values.md)

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt, wie der dritte Parameter (P3)-Byte aus der [*Application Protocol Data Unit*](../secgloss/a-gly.md) (APDU) abgerufen wird. Im Beispiel wird davon ausgegangen, dass pISCardCmd ein gültiger Zeiger auf eine Instanz der [**ISCardCmd-Schnittstelle**](iscardcmd.md) ist.


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
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                   |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>Ddat.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Ddat.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardCmd ist als D5778AE3-43DE-11D0-9171-00AA00C18068 definiert.<br/>            |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_P1 abrufen**](iscardcmd-get-p1.md)
</dt> <dt>

[**\_P2 abrufen**](iscardcmd-get-p2.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> </dl>

 

 
