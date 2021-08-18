---
description: Die SetDefaultClassId-Methode weist ein Standardklassenbezeichner-Byte zu, das bei der Erstellung einer ISO 7816-4-Befehlsanwendungsprotokoll-Dateneinheit (APDU) in allen Vorgängen verwendet wird. Standardmäßig ist das Standardklassenbezeichner-Byte 0x00.
ms.assetid: 5a53d5f1-7986-4c4c-9512-f592cd398d1c
title: ISCardISO7816::SetDefaultClassId-Methode (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.SetDefaultClassId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: d242d83af00bb0d8e10d7da22d014a31deafaa66f49fb509cc91b65263239dd4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119481114"
---
# <a name="iscardiso7816setdefaultclassid-method"></a>ISCardISO7816::SetDefaultClassId-Methode

\[Die **SetDefaultClassId-Methode** ist für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **SetDefaultClassId-Methode** weist ein Standardklassenbezeichner-Byte zu, das bei der Erstellung einer ISO 7816-4-Befehlsanwendungsprotokoll-Dateneinheit (APDU) in allen Vorgängen verwendet wird. [](../secgloss/a-gly.md) Standardmäßig ist das Standardklassenbezeichner-Byte 0x00.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetDefaultClassId(
  [in] BYTE byClass
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*byClass* \[ In\]
</dt> <dd>

Klassen-ID-Byte.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Folgende Rückgabewerte sind möglich:



| Rückgabecode                                                                          | Beschreibung                                  |
|--------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Operation erfolgreich abgeschlossen.<br/> |



 

Eine Liste aller Methoden, die von der [**ISCardISO7816-Schnittstelle**](iscardiso7816.md) bereitgestellt werden, finden Sie unter **ISCardISO7816.**

Zusätzlich zu den oben aufgeführten COM-Fehlercodes kann diese Schnittstelle einen [*Smartcardfehlercode*](../secgloss/s-gly.md) zurückgeben, wenn eine Smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen. Informationen zu Smartcard-Fehlercodes finden Sie unter [Smartcard-Rückgabewerte.](authentication-return-values.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                   |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>Scardssp.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Scardsrv.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardISO7816 ist als 53B6AA68-3F56-11D0-916B-00AA00C18068 definiert.<br/>        |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> </dl>

 

 
