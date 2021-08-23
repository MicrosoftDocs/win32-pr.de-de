---
description: Gibt einen neuen alternativen Klassenbezeichner in der Application Protocol Data Unit (APDU) an.
ms.assetid: 45a49699-41ce-439c-b896-e663a290b188
title: ISCardCmd::p ut_AlternateClassId-Methode (Discountddat.h)
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
ms.openlocfilehash: fd1f74dee017cb72a67ecb4a9fc42da85153966336b25e54819be13464b3b7e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119481560"
---
# <a name="iscardcmdput_alternateclassid-method"></a>ISCardCmd::p ut \_ AlternateClassId-Methode

\[Die **\_ put AlternateClassId-Methode** steht für die Verwendung in den Betriebssystemen zur Verfügung, die im Abschnitt Anforderungen angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **put \_ AlternateClassId-Methode** gibt einen neuen alternativen Klassenbezeichner in der [*Application Protocol Data Unit*](../secgloss/a-gly.md) (APDU) an.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_AlternateClassId(
  [in] BYTE byClass
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*byClass* \[ In\]
</dt> <dd>

Alternativer Klassenbezeichner. Der Standardwert ist 0 (null).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                  | Beschreibung                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Operation erfolgreich abgeschlossen.<br/>     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Der *byClass-Parameter* ist ungültig.<br/> |



 

## <a name="remarks"></a>Hinweise

Bei der Kommunikation mit dem [*T=0-Protokoll*](../secgloss/t-gly.md)können zusätzliche Kartenbefehle automatisch von der APDU generiert und an die Übertragungsprotokoll-Dateneinheit (TPDU) gesendet werden. Die zusätzlichen Befehle verwenden in der Regel die gleiche Klassen-ID wie der ursprüngliche Befehl. Durch das Angeben einer neuen Klassen-ID mithilfe dieser Methode können automatisch generierte Befehle die neue Klassen-ID verwenden.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt, wie sie einen neuen alternativen Klassenbezeichner in der [*Anwendungsprotokolldateneinheit*](../secgloss/a-gly.md) (APPLICATION Protocol Data Unit, APDU) festlegen. Im Beispiel wird davon ausgegangen, dass pISCardCmd ein gültiger Zeiger auf eine Instanz der [**ISCardCmd-Schnittstelle**](iscardcmd.md) ist.


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

[**ISCardCmd**](iscardcmd.md)
</dt> <dt>

[**Get \_ AlternateClassId**](iscardcmd-get-alternateclassid.md)
</dt> </dl>

 

 
