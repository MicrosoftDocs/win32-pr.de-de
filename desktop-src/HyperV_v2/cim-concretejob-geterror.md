---
description: Ruft einen Fehler aufgrund eines fehlgeschlagenen Auftrags ab.
ms.assetid: d499eb91-e1cc-4792-b32d-5a8875eebbb7
title: GetError-Methode der CIM_ConcreteJob-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConcreteJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: aa9ed87f2d484286d91d14c4183d2ce3b6f41cfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345166"
---
# <a name="geterror-method-of-the-cim_concretejob-class"></a>GetError-Methode der CIM- \_ Klasse "concretejob"

Ruft einen Fehler aufgrund eines fehlgeschlagenen Auftrags ab. Wenn der Auftrag ausgeführt wird oder ohne Fehler beendet wurde, gibt diese Methode keine [**CIM- \_ Fehler**](cim-error.md) Instanz zurück. Wenn der Auftrag jedoch aufgrund eines internen Problems fehlgeschlagen ist oder der Auftrag von einem Client beendet wurde, wird eine **CIM- \_ Fehler** Instanz zurückgegeben.

## <a name="syntax"></a>Syntax


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Fehler* \[ vorgenommen\]
</dt> <dd>

Gibt eine [**CIM- \_ Fehler**](cim-error.md) Instanz zurück, wenn der **OperationalStatus** für den Auftrag nicht "OK" ist; andernfalls wird **null** zurückgegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 (null) zurück. Andernfalls wird ein Fehler zurückgegeben.

<dl> <dt>

**Erfolg** (0)
</dt> <dt>

**Nicht unterstützt** (1)
</dt> <dt>

**Nicht spezifizierter Fehler** (2)
</dt> <dt>

**Timeout** (3)
</dt> <dt>

Fehler **(4** )
</dt> <dt>

**Ungültiger Parameter** (5)
</dt> <dt>

**Zugriff verweigert** (6)
</dt> <dt>

**DMTF reserviert** (..)
</dt> <dt>

**Hersteller spezifisch** (32768.65535)
</dt> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1<br/>                                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ concretejob**](cim-concretejob.md)
</dt> </dl>

 

 




