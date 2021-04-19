---
description: Aktualisiert das übergeordnete Element für das angegebene Blatt und die untergeordneten virtuellen Festplatten Dateien.
ms.assetid: 5ad41218-bcfd-449a-a66e-2096a1d96bf5
title: Setparameentvirtualharddisk-Methode der Msvm_ImageManagementService-Klasse
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
ms.openlocfilehash: f1d14d3b2ee19a9768e1ee9ed9333a452153cc9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349400"
---
# <a name="setparentvirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a>Setparameentvirtualharddisk-Methode der MSVM \_ imagemanagementservice-Klasse

Aktualisiert das übergeordnete Element für das angegebene Blatt und die untergeordneten virtuellen Festplatten Dateien. Weitere Informationen zu Nutzungseinschränkungen für diese Methode finden Sie unter Hinweise.

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

*Childpath* \[ in\]
</dt> <dd>

Ein voll qualifizierter Pfad, der den Speicherort der untergeordneten virtuellen Festplatten Datei angibt.

</dd> <dt>

Element *Pfad* \[ in\]
</dt> <dd>

Ein voll qualifizierter Pfad, der den Speicherort der übergeordneten virtuellen Festplatten Datei angibt.

</dd> <dt>

*Blattpfad* \[ in\]
</dt> <dd>

Ein voll qualifizierter Pfad, der den Speicherort der virtuellen Festplatten Datei für das Blatt angibt. Der-Parameter kann **null** sein, wenn die virtuelle Festplatte offline ist, muss jedoch angegeben werden, wenn die virtuelle Festplatte verwendet wird.

</dd> <dt>

*Ignoreidmismatch* \[ in\]
</dt> <dd>

Gibt an, ob das übergeordnete Element zwangsweise festgelegt werden soll, wenn die IDs der virtuellen Datenträger nicht stimmen. Dieser Parameter muss mit Bedacht verwendet werden, denn wenn die neue übergeordnete virtuelle Festplatte nicht mit der ursprünglichen übergeordneten Festplatte identisch ist, können Daten beschädigt werden.

</dd> <dt>

*Auftrag* \[ vorgenommen\]
</dt> <dd>

Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück.

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)
</dt> <dt>

Fehler **(32768** )
</dt> <dt>

**Zugriff verweigert** (32769)
</dt> <dt>

**Nicht unterstützt** (32770)
</dt> <dt>

Der **Status ist "Unknown** " (32771).
</dt> <dt>

**Timeout** (32772)
</dt> <dt>

**Ungültiger Parameter** (32773)
</dt> <dt>

**System wird verwendet** (32774)
</dt> <dt>

**Ungültiger Status für diesen Vorgang** (32775).
</dt> <dt>

**Falscher Datentyp** (32776).
</dt> <dt>

Das **System ist nicht verfügbar** (32777).
</dt> <dt>

**Nicht** genügend Arbeitsspeicher (32778)
</dt> <dt>

Die **Datei wurde nicht gefunden** (32779).
</dt> </dl>

## <a name="remarks"></a>Bemerkungen

Mit dieser Methode können nur die folgenden Typen von virtuellen Festplatten verwendet werden:

-   Differenzierende VHD
-   Differenzierende vhdx

Der Zugriff auf die [**MSVM \_ imagemanagementservice**](msvm-imagemanagementservice.md) -Klasse kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MSVM \_ imagemanagementservice**](msvm-imagemanagementservice.md)
</dt> </dl>

 

