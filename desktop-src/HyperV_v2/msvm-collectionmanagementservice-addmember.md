---
description: Fügt das angegebene verwaltete Element als Member des angegebenen CIM \_ CollectionOfMSEs-Objekts hinzu.
ms.assetid: 6f23eecc-b445-4495-ae96-76b89652a1cb
title: AddMember-Methode der Msvm_CollectionManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService.AddMember
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6b885701086262fda48c5d50abd750eca6866c72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760500"
---
# <a name="addmember-method-of-the-msvm_collectionmanagementservice-class"></a>AddMember-Methode der MSVM \_ collectionmanagementservice-Klasse

Fügt das angegebene verwaltete Element als Member des angegebenen [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) -Objekts hinzu.

## <a name="syntax"></a>Syntax


```mof
uint32 AddMember(
  [in]  CIM_ManagedElement   REF Member,
  [in]  CIM_CollectionOfMSEs REF Collection,
  [out] CIM_ConcreteJob      REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Mitglied* \[ in\]
</dt> <dd>

Der Member, der der Auflistung hinzugefügt werden soll.

</dd> <dt>

*Sammlung* \[ in\]
</dt> <dd>

Die Auflistung, der das Element hinzugefügt werden soll.

</dd> <dt>

*Auftrag* \[ vorgenommen\]
</dt> <dd>

Ein Verweis auf den Auftrag (kann NULL sein, wenn die Aufgabe abgeschlossen ist).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 zurück, wenn erfolgreich, oder 4096, wenn der Auftrag gestartet wurde. Andernfalls wird ein Fehler zurückgegeben.

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

[**MSVM \_ collectionmanagementservice**](msvm-collectionmanagementservice.md)
</dt> </dl>

 

 




