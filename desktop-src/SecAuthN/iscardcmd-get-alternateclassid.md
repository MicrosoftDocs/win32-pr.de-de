---
description: Ruft den Wert der alternativen Klassen-ID ab.
ms.assetid: 80c7cbba-e28d-4973-9f3f-7636ff331b64
title: ISCardCmd::get_AlternateClassId-Methode (Scarddat.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_AlternateClassId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ac6d74f89eaf2c42ec9fc00cef9d82735b4b28885180c3c5d429dad7450e3c74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119577780"
---
# <a name="iscardcmdget_alternateclassid-method"></a>ISCardCmd::get \_ AlternateClassId-Methode

\[Die **Get \_ AlternateClassId-Methode** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **Get \_ AlternateClassId-Methode** ruft den Wert der alternativen Klassen-ID ab. Bei dieser Methode ist ein Fehler zu sehen, es sei denn, die alternative ID wurde durch einen vorherigen Aufruf von [**\_ AlternateClassId festgelegt.**](iscardcmd-put-alternateclassid.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT get_AlternateClassId(
  [out] BYTE *pbyClass
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pbyClass* \[ out\]
</dt> <dd>

Zeiger auf das Byte, das den alternativen Klassen-ID-Wert bei der Rückgabe enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt die folgenden möglichen Werte zurück.



| Rückgabecode                                                                                    | Beschreibung                                                                                                                                 |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Der Vorgang wurde erfolgreich abgeschlossen.<br/>                                                                                            |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>   | Der *pbyClass-Parameter* ist ungültig.<br/>                                                                                           |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Die alternative Klassen-ID wurde zuvor nicht durch einen Aufruf von [**\_ AlternateClassId festgelegt.**](iscardcmd-put-alternateclassid.md)<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Methode gilt für die Kommunikation mithilfe des [*T=0-Protokolls*](../secgloss/t-gly.md). Weitere Informationen finden Sie unter [**put \_ AlternateClassId**](iscardcmd-put-alternateclassid.md).

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt, wie die alternative Klassen-ID abgerufen wird. Im Beispiel wird davon ausgegangen, dass pISCardCmd ein gültiger Zeiger auf eine Instanz der [**ISCardCmd-Schnittstelle**](iscardcmd.md) ist.


```C++
BYTE     byAltClassID;
HRESULT  hr;

// Retrieve the alternate class ID.
hr = pISCardCmd->get_AlternateClassId(&byAltClassID);
if (FAILED(hr))
{
  printf("Failed get_AltClassId\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                   |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>Scarddat.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Scarddat.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardCmd ist als D5778AE3-43DE-11D0-9171-00AA00C18068 definiert.<br/>            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> <dt>

[**put \_ AlternateClassId**](iscardcmd-put-alternateclassid.md)
</dt> </dl>

 

 
