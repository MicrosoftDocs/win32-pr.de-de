---
title: Setvirtualdesktopstate-Methode der Win32_RDMSVirtualDesktop-Klasse
description: Aktualisiert den Zustand des virtuellen Desktops.
ms.assetid: 8f4f3d31-0434-4018-a33a-2ffd62c09669
ms.tgt_platform: multiple
keywords:
- Setvirtualdesktopstate-Methode Remotedesktopdienste
- Setvirtualdesktopstate-Methode Remotedesktopdienste, Win32_RDMSVirtualDesktop-Klasse
- Win32_RDMSVirtualDesktop-Klasse Remotedesktopdienste, setvirtualdesktopstate-Methode
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
ms.openlocfilehash: af913e29857a59cacf283bff6a1642e0ea4cef9d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344679"
---
# <a name="setvirtualdesktopstate-method-of-the-win32_rdmsvirtualdesktop-class"></a>Setvirtualdesktopstate-Methode der Win32 \_ -Klasse rdmsvirtualdesktop

Aktualisiert den Zustand des virtuellen Desktops.

## <a name="syntax"></a>Syntax


```mof
uint32 SetVirtualDesktopState(
  [in] uint32 VMState
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Vmstate* \[ in\]
</dt> <dd>

Ein-Wert, der den neuen Zustand des virtuellen Computers angibt.

Mit diesem Parameter kann auf einen der folgenden Werte festgelegt werden:

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0 (Standard))


</dt> <dd>

Der Status der virtuellen Maschine konnte nicht ermittelt werden.

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (2)


</dt> <dd>

Der virtuelle Computer wird ausgeführt.

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (3)


</dt> <dd>

Der virtuelle Computer ist ausgeschaltet.

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (32768)


</dt> <dd>

Der virtuelle Computer wurde angehalten.

</dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>Angeh **alten (32769** )


</dt> <dd>

Der virtuelle Computer befindet sich in einem gespeicherten Zustand.

</dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>Wird **gestartet** (32770)


</dt> <dd>

Der virtuelle Computer wird gestartet.

</dd> <dt>

<span id="Saving"></span><span id="saving"></span><span id="SAVING"></span>

<span id="Saving"></span><span id="saving"></span><span id="SAVING"></span>Wird **gespeichert** (32773)


</dt> <dd>

Der virtuelle Computer speichert seinen Zustand.

</dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>Wird **beendet (32774** )


</dt> <dd>

Der virtuelle Computer wird ausgeschaltet.

</dd> <dt>

<span id="Pausing"></span><span id="pausing"></span><span id="PAUSING"></span>

<span id="Pausing"></span><span id="pausing"></span><span id="PAUSING"></span>Wird **angeh** alten (32776)


</dt> <dd>

Der virtuelle Computer wird angehalten.

</dd> <dt>

<span id="Resuming"></span><span id="resuming"></span><span id="RESUMING"></span>

<span id="Resuming"></span><span id="resuming"></span><span id="RESUMING"></span>Wird fort **gesetzt (32777** )


</dt> <dd>

Der virtuelle Computer wird von einem angehaltenen Zustand fortgesetzt.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                              |
| Namespace<br/>                | Root \\ CIMv2 \\ RDMs<br/>                                                                |
| MOF<br/>                      | <dl> <dt>Rdmanagement. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ rdmsvirtualdesktop**](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





