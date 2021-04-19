---
description: Ruft Informationen zu einer VHD-Datei ab.
ms.assetid: efdfd4c6-b762-4369-add3-e152652c6802
title: Getvhdsetinformation-Methode der Msvm_ImageManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.GetVHDSetInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 16cdcf4a354e6d6b47b6a67c071daf8883905f12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348209"
---
# <a name="getvhdsetinformation-method-of-the-msvm_imagemanagementservice-class"></a>Getvhdsetinformation-Methode der MSVM \_ imagemanagementservice-Klasse

Ruft Informationen zu einer VHD-Datei ab.

## <a name="syntax"></a>Syntax


```mof
uint32 GetVHDSetInformation(
  [in]  string              VHDSetPath,
  [in]  uint32              AdditionalInformation[],
  [out] string              Information,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Vhdsetpath* \[ in\]
</dt> <dd>

Ein voll qualifizierter Pfad, der den Speicherort der VHD-Satz Datei angibt.

</dd> <dt>

*AdditionalInformation* \[ in\]
</dt> <dd>

Ein Array, das angibt, welche zusätzlichen Informationen über die VHD-Satz Datei erfasst werden sollen. Jeder Eintrag im Array ist ein Typ zusätzlicher Informationen. Wenn dieser Parameter NULL ist, werden keine zusätzlichen Informationen abgerufen.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="Paths"></span><span id="paths"></span><span id="PATHS"></span>

**Pfade** (2)


</dt> <dd></dd> </dl> </dd> <dt>

*Informationen* \[ vorgenommen\]
</dt> <dd>

Bei erfolgreicher Ausführung enthält dieses Objekt die Informationen für die angeforderte VHD-Satz Datei. Dabei handelt es sich um eine eingebettete Instanz von [**MSVM \_ vhdsetinformation**](msvm-vhdsetinformation.md).

</dd> <dt>

*Auftrag* \[ vorgenommen\]
</dt> <dd>

Ein Verweis auf den Auftrag (kann NULL sein, wenn die Aufgabe abgeschlossen ist).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück:

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

[**MSVM \_ imagemanagementservice**](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




