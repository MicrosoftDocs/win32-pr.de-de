---
title: SetVirtualDesktopState-Methode der Win32_RDMSVirtualDesktop Klasse
description: Aktualisiert den Status des virtuellen Desktops.
ms.assetid: 8f4f3d31-0434-4018-a33a-2ffd62c09669
ms.tgt_platform: multiple
keywords:
- SetVirtualDesktopState-Remotedesktopdienste
- SetVirtualDesktopState-Methode Remotedesktopdienste , Win32_RDMSVirtualDesktop-Klasse
- Win32_RDMSVirtualDesktop klasse Remotedesktopdienste , SetVirtualDesktopState-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.SetVirtualDesktopState
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b970f70996d5052674949f7ae6c89d71cbf69dc0ac90df46caaf975f8a1e279
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058438"
---
# <a name="setvirtualdesktopstate-method-of-the-win32_rdmsvirtualdesktop-class"></a>SetVirtualDesktopState-Methode der Win32 \_ RDMSVirtualDesktop-Klasse

Aktualisiert den Status des virtuellen Desktops.

## <a name="syntax"></a>Syntax


```mof
uint32 SetVirtualDesktopState(
  [in] uint32 VMState
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*VMState* \[ In\]
</dt> <dd>

Ein -Wert, der den neuen Zustand des virtuellen Computers angibt.

Dieser Parameter kann auf einen der folgenden Werte festgelegt werden:

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0 (Standard))


</dt> <dd>

Der Status des virtuellen Computers konnte nicht bestimmt werden.

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (2)


</dt> <dd>

Der virtuelle Computer wird ausgeführt.

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (3)


</dt> <dd>

Der virtuelle Computer ist deaktiviert.

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angehalten** (32768)


</dt> <dd>

Der virtuelle Computer wird angehalten.

</dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Angehalten** (32769)


</dt> <dd>

Der virtuelle Computer befindet sich in einem gespeicherten Zustand.

</dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Ab** (32770)


</dt> <dd>

Der virtuelle Computer wird gestartet.

</dd> <dt>

<span id="Saving"></span><span id="saving"></span><span id="SAVING"></span>

<span id="Saving"></span><span id="saving"></span><span id="SAVING"></span>**Speichern** (32773)


</dt> <dd>

Der virtuelle Computer wird seinen Zustand speichern.

</dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Wird** beendet (32774)


</dt> <dd>

Der virtuelle Computer wird ausgeschaltet.

</dd> <dt>

<span id="Pausing"></span><span id="pausing"></span><span id="PAUSING"></span>

<span id="Pausing"></span><span id="pausing"></span><span id="PAUSING"></span>**Anhalten** (32776)


</dt> <dd>

Der virtuelle Computer wird pausiert.

</dd> <dt>

<span id="Resuming"></span><span id="resuming"></span><span id="RESUMING"></span>

<span id="Resuming"></span><span id="resuming"></span><span id="RESUMING"></span>**Fortsetzen** (32777)


</dt> <dd>

Der virtuelle Computer wird aus einem angehaltenen Zustand fortsetzen.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                              |
| Namespace<br/>                | \\Stamm-CIMv2-Rdms \\<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ RDMSVirtualDesktop**](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





