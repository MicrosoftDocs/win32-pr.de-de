---
description: Ruft die aktuelle Größe des freien virtuellen Adressraums in Bytes ab, der für den Prozess verfügbar ist.
ms.assetid: 13b3b347-5db1-484f-bd1d-3a604eb6bc5b
ms.tgt_platform: multiple
title: Getavailablevirtualsize-Methode der Win32_Process-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.GetAvailableVirtualSize
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ee6e798b8df32822de481f3af1dc6b21a81d1024
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344351"
---
# <a name="getavailablevirtualsize-method-of-the-win32_process-class"></a>Getavailablevirtualsize-Methode der Win32- \_ Prozess Klasse

Ruft die aktuelle Größe des freien virtuellen Adressraums in Bytes ab, der für den Prozess verfügbar ist.

## <a name="syntax"></a>Syntax


```mof
uint32 GetAvailableVirtualSize(
  [out] uint64 AvailableVirtualSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Availablevirtualsize* \[ vorgenommen\]
</dt> <dd>

Der *availablevirtualsize* -Parameter gibt den freien virtuellen Adressraum zurück, der für diesen Prozess verfügbar ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt NULL (0) zurück, um den Erfolg anzugeben. Jede andere Zahl gibt einen Fehler an. Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Erfolgreicher Abschluss**
</dt> <dd>

0

Der Vorgang wurde erfolgreich abgeschlossen.

</dd> <dt>

**Zugriff verweigert**
</dt> <dd>

2

Der Benutzer hat keinen Zugriff auf die angeforderten Informationen.

</dd> <dt>

**Unzureichende Berechtigungen**
</dt> <dd>

3

Der Benutzer verfügt nicht über ausreichende Berechtigungen.

</dd> <dt>

**Unbekannter Fehler.**
</dt> <dd>

8

Unbekannter Fehler.

</dd> <dt>

**Der Pfad wurde nicht gefunden**
</dt> <dd>

9

Der angegebene Pfad ist nicht vorhanden.

</dd> <dt>

**Ungültiger Parameter**
</dt> <dd>

21

Der angegebene Parameter ist ungültig.

</dd> <dt>

**Andere**
</dt> <dd>

22 4294967295

Weitere Werte als die aufgeführten Werte finden Sie in der Dokumentation zu [System Fehler Codes](/windows/desktop/Debug/system-error-codes) .

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1<br/>                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                       |
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ Prozess**](win32-process.md)
</dt> </dl>

 

