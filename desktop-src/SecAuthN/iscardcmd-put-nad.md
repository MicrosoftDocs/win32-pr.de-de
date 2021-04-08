---
description: Gibt die Knotenadresse (nad) an, die mit der iscardcmd-Schnittstelle verwendet werden soll.
ms.assetid: 49de8264-9491-41a4-a8e0-68d0db088ded
title: Iscardcmd::p ut_Nad-Methode (scarddat. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_Nad
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 64ed9c502811db5666e561a1f290cc234e6c81e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863264"
---
# <a name="iscardcmdput_nad-method"></a>Iscardcmd::p UT \_ nad-Methode

\[Die **Put \_ nad** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die **Put \_ nad** -Methode gibt die Knotenadresse (nad) an, die mit der [**iscardcmd**](iscardcmd.md) -Schnittstelle verwendet werden soll. Dies gilt für die Kommunikation, die nur die [*Protokoll Kommunikation T = 1*](../secgloss/t-gly.md) verwendet. Standardmäßig verwendet das [**iscardcmd**](iscardcmd.md) -Objekt einen nad-Wert von 0 (null).

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Nad(
  [in] BYTE bNad
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bnad* \[ in\]
</dt> <dd>

Byte, das das zu verwendende nad darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                  | Beschreibung                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Der Vorgang wurde erfolgreich abgeschlossen.<br/> |
| <dl> <dt>**E \_ invalidArg**</dt> </dl> | Der *bnad* -Parameter ist ungültig.<br/>    |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode sollte nur aufgerufen werden, wenn es erforderlich ist, einen anderen Wert als 0 (null) für die nad zu verwenden.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird gezeigt, wie eine mit der [**iscardcmd**](iscardcmd.md) -Schnittstelle zu verwendende Knotenadresse angegeben wird. Im Beispiel wird davon ausgegangen, dass bynadvalue eine Variable vom Typ " **Byte** " ist, der zuvor ein Wert zugewiesen wurde, und dass "piscardcmd" ein gültiger Zeiger auf eine Instanz der **iscardcmd** -Schnittstelle ist.


```C++
HRESULT  hr;

// Set the Nad.
// byNadValue is a previously assigned BYTE value.
hr = pISCardCmd->put_Nad(byNadValue);
if (FAILED(hr))
{
  printf("Failed put_Nad\n");
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
</dt> </dl>

 

 
