---
description: Gibt einen neuen alternativen Klassen Bezeichner in APDU (Application Protocol Data Unit) an.
ms.assetid: 45a49699-41ce-439c-b896-e663a290b188
title: Iscardcmd::p ut_AlternateClassId-Methode (scarddat. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_AlternateClassId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ee1ee5da5875ec2fa1f4f7f6e474f551befdaf8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343306"
---
# <a name="iscardcmdput_alternateclassid-method"></a>Iscardcmd::p UT \_ -Methode "alternative Methode"

\[Die **Put \_ -** Methode "Alternativen" ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die **Put Alternate \_ eclassid-** Methode gibt einen neuen alternativen Klassen Bezeichner in der [*Anwendungsprotokoll Daten-Einheit*](../secgloss/a-gly.md) (APDU) an.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_AlternateClassId(
  [in] BYTE byClass
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*byclass* \[ in\]
</dt> <dd>

Alternativer Klassen Bezeichner. Der Standardwert ist 0 (null).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                  | Beschreibung                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Operation erfolgreich abgeschlossen.<br/>     |
| <dl> <dt>**E \_ invalidArg**</dt> </dl> | Der *byclass* -Parameter ist ungültig.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Bei der Kommunikation mit dem [*T = 0-Protokoll*](../secgloss/t-gly.md)können zusätzliche Karten Befehle automatisch von APDU generiert und an die Übertragungsprotokoll-Dateneinheit gesendet werden. Die zusätzlichen Befehle verwenden normalerweise dieselbe Klassen-ID wie der ursprüngliche Befehl. durch die Angabe einer neuen Klassen-ID mithilfe dieser Methode können automatisch generierte Befehle die neue Klassen-ID verwenden.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird gezeigt, wie Sie einen neuen alternativen Klassen Bezeichner in der [*Anwendungsprotokoll Daten-Einheit (Application Protocol Data Unit*](../secgloss/a-gly.md) , APDU) festlegen. Im Beispiel wird davon ausgegangen, dass "piscardcmd" ein gültiger Zeiger auf eine Instanz der [**iscardcmd**](iscardcmd.md) -Schnittstelle ist.


```C++
HRESULT  hr;

// Set the class ID.
hr = pISCardCmd->put_AlternateClassId(0xC0);
if (FAILED(hr))
{
  printf("Failed put_AlternateClassId\n");
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

[**Iscardcmd**](iscardcmd.md)
</dt> <dt>

[**\_Alternative zum abwechseln**](iscardcmd-get-alternateclassid.md)
</dt> </dl>

 

 
