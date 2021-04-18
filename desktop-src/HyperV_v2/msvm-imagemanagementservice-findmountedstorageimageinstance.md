---
description: Sucht ein MSVM \_ mountedstorageimage-Objekt für einen angegebenen Datenträger-Bildpfad.
ms.assetid: 498ed285-2b5b-472b-b0ee-649c97b61274
title: Findmountedstorageimageinstance-Methode der Msvm_ImageManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.FindMountedStorageImageInstance
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 80462fb57be8c3f89764774ea68e73a988f11643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526834"
---
# <a name="findmountedstorageimageinstance-method-of-the-msvm_imagemanagementservice-class"></a>Findmountedstorageimageinstance-Methode der MSVM \_ imagemanagementservice-Klasse

Sucht ein [**MSVM \_ mountedstorageimage**](msvm-mountedstorageimage.md) -Objekt für einen angegebenen Datenträger-Bildpfad.

## <a name="syntax"></a>Syntax


```mof
uint32 FindMountedStorageImageInstance(
  [in]  string                       SelectionCriterion,
  [in]  uint16                       CriterionType,
  [out] Msvm_MountedStorageImage REF Image
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Selectionkriterium* \[ in\]
</dt> <dd>

Ein voll qualifizierter Pfad, der den Speicherort einer Datenträger Image Datei angibt.

</dd> <dt>

*Kriteriontype* \[ in\]
</dt> <dd>

Der Typ des Kriteriums, das beim Auffinden des Datenträger Images gesucht werden soll.

<dt>

<span id="unknown"></span><span id="UNKNOWN"></span>

**unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Path"></span><span id="path"></span><span id="PATH"></span>

**Pfad** (2)


</dt> <dd></dd> </dl> </dd> <dt>

*Bild* \[ vorgenommen\]
</dt> <dd>

Ein Verweis auf [**MSVM \_ mountedstorageimage**](msvm-mountedstorageimage.md) (kann NULL sein, wenn das Bild nicht eingebunden ist).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück:

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
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
</dt> <dt>

**Objekt nicht gefunden** (32789)
</dt> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MSVM \_ imagemanagementservice**](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




