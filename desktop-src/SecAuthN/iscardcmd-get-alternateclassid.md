---
description: Ruft den Wert der alternativen Klassen-ID ab.
ms.assetid: 80c7cbba-e28d-4973-9f3f-7636ff331b64
title: 'Iscardcmd:: get_AlternateClassId-Methode (scarddat. h)'
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
ms.openlocfilehash: 8cfc47011881ae3e3f6df5ef51c910899a054f84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363335"
---
# <a name="iscardcmdget_alternateclassid-method"></a>Iscardcmd:: get- \_ Methode "alternative Methode"

\[Die Methode " **get \_ Alternativen Klassifizierungs d** " ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die Methode **Get Alternate \_ -lassid** Ruft den Wert der alternativen Klassen-ID ab. Bei dieser Methode tritt ein Fehler auf, es sei [**denn, die \_**](iscardcmd-put-alternateclassid.md)Alternative ID wurde durch einen vorherigen-Befehl von Set Alternate

## <a name="syntax"></a>Syntax


```C++
HRESULT get_AlternateClassId(
  [out] BYTE *pbyClass
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pbyclass* \[ vorgenommen\]
</dt> <dd>

Zeiger auf das Byte, das bei Rückgabe den Wert der alternativen Klassen-ID enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt die folgenden möglichen Werte zurück.



| Rückgabecode                                                                                    | Beschreibung                                                                                                                                 |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Der Vorgang wurde erfolgreich abgeschlossen.<br/>                                                                                            |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>   | Der *pbyclass* -Parameter ist ungültig.<br/>                                                                                           |
| <dl> <dt>**E \_ AccessDenied**</dt> </dl> | Die Alternative Klassen-ID wurde zuvor nicht durch einen-Befehl zum Einfügen von ' Alternate [**\_ -lassid**](iscardcmd-put-alternateclassid.md)' festgelegt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode gilt für die Kommunikation mit dem [*Protokoll T = 0*](../secgloss/t-gly.md). Weitere Informationen finden Sie unter [**Put \_ -Alternativen**](iscardcmd-put-alternateclassid.md).

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird gezeigt, wie die Alternative Klassen-ID abgerufen wird. Im Beispiel wird davon ausgegangen, dass "piscardcmd" ein gültiger Zeiger auf eine Instanz der [**iscardcmd**](iscardcmd.md) -Schnittstelle ist.


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

[**" \_ Alternative" platzieren**](iscardcmd-put-alternateclassid.md)
</dt> </dl>

 

 
