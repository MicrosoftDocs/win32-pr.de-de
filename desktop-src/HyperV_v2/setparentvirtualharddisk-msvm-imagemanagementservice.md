---
description: Aktualisiert das übergeordnete Element für die angegebenen untergeordneten und untergeordneten virtuellen Festplattendateien.
ms.assetid: 5ad41218-bcfd-449a-a66e-2096a1d96bf5
title: SetParentVirtualHardDisk-Methode der Msvm_ImageManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.SetParentVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 47be9f3f383da237a3679633ac1d663bbc81ef078a7529662b8f21d10246761f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050540"
---
# <a name="setparentvirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a>SetParentVirtualHardDisk-Methode der Msvm \_ ImageManagementService-Klasse

Aktualisiert das übergeordnete Element für die angegebenen untergeordneten und untergeordneten virtuellen Festplattendateien. Informationen zu Verwendungseinschränkungen für diese Methode finden Sie unter Hinweise.

## <a name="syntax"></a>Syntax


```mof
uint32 SetParentVirtualHardDisk(
  [in]  string              ChildPath,
  [in]  string              ParentPath,
  [in]  string              LeafPath,
  [in]  boolean             IgnoreIDMismatch,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ChildPath* \[ In\]
</dt> <dd>

Ein vollqualifizierten Pfad, der den Speicherort der untergeordneten virtuellen Festplattendatei angibt.

</dd> <dt>

*ParentPath* \[ In\]
</dt> <dd>

Ein vollqualifizierten Pfad, der den Speicherort der übergeordneten virtuellen Festplattendatei angibt.

</dd> <dt>

*LeafPath* \[ In\]
</dt> <dd>

Ein vollqualifizierten Pfad, der den Speicherort der virtuellen Blattfestplattedatei angibt. Der Parameter kann **NULL** sein, wenn die virtuelle Festplatte offline ist, aber angegeben werden muss, wenn die virtuelle Festplatte verwendet wird.

</dd> <dt>

*IgnoreIDMismatch* \[ In\]
</dt> <dd>

Gibt an, ob das übergeordnete Element festgelegt werden soll, wenn die Bezeichner des virtuellen Datenträgers nicht übereinstimmen. Dieser Parameter muss mit Vorsicht verwendet werden, da datenbeschädigungen auftreten können, wenn die neue übergeordnete virtuelle Festplatte nicht mit der ursprünglichen übergeordneten Festplatte identisch ist.

</dd> <dt>

*Auftrag* \[ out\]
</dt> <dd>

Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein objekt, das von [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))abgeleitet wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück.

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

**Überprüfte Methodenparameter – Auftragsstart** (4096)
</dt> <dt>

**Fehler** (32768)
</dt> <dt>

**Zugriff verweigert** (32769)
</dt> <dt>

**Nicht unterstützt** (32770)
</dt> <dt>

**Status ist unbekannt** (32771)
</dt> <dt>

**Timeout** (32772)
</dt> <dt>

**Ungültiger Parameter** (32773)
</dt> <dt>

**System wird verwendet** (32774)
</dt> <dt>

**Ungültiger Zustand für diesen Vorgang** (32775)
</dt> <dt>

**Falscher Datentyp** (32776)
</dt> <dt>

**System ist nicht verfügbar** (32777)
</dt> <dt>

**Nicht genügend Arbeitsspeicher** (32778)
</dt> <dt>

**Datei nicht gefunden** (32779)
</dt> </dl>

## <a name="remarks"></a>Hinweise

Mit dieser Methode können nur die folgenden Arten von virtuellen Festplatten verwendet werden:

-   Differenzierende VHD
-   Differenzierende VHDX

Der Zugriff auf die [**Msvm \_ ImageManagementService-Klasse**](msvm-imagemanagementservice.md) kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msvm \_ ImageManagementService**](msvm-imagemanagementservice.md)
</dt> </dl>

 

