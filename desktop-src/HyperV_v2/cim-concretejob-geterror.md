---
description: Ruft einen Fehler aufgrund eines fehlgeschlagenen Auftrags ab.
ms.assetid: d499eb91-e1cc-4792-b32d-5a8875eebbb7
title: GetError-Methode der CIM_ConcreteJob Klasse
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
ms.openlocfilehash: 0b43d433bf9d2a3967efcc4a2e927d3bf687ebfa5ac67d7c7e34c48c34832c26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117813266"
---
# <a name="geterror-method-of-the-cim_concretejob-class"></a>GetError-Methode der CIM \_ ConcreteJob-Klasse

Ruft einen Fehler aufgrund eines fehlgeschlagenen Auftrags ab. Wenn der Auftrag ausgeführt wird oder ohne Fehler beendet wurde, gibt diese Methode keine [**\_ CIM-Fehlerinstanz**](cim-error.md) zurück. Wenn der Auftrag jedoch aufgrund eines internen Problems fehlgeschlagen ist oder weil der Auftrag von einem Client beendet wurde, wird eine **\_ CIM-Fehlerinstanz** zurückgegeben.

## <a name="syntax"></a>Syntax


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Fehler* \[ out\]
</dt> <dd>

Gibt eine [**\_ CIM-Fehlerinstanz**](cim-error.md) zurück, wenn **operationalStatus** für den Auftrag nicht "OK" ist. Andernfalls wird **NULL zurückgegeben.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg eine 0 zurück. andernfalls gibt einen Fehler zurück.

<dl> <dt>

**Erfolg** (0)
</dt> <dt>

**Nicht unterstützt** (1)
</dt> <dt>

**Nicht angegebener Fehler** (2)
</dt> <dt>

**Timeout** (3)
</dt> <dt>

**Fehler** (4)
</dt> <dt>

**Ungültiger Parameter** (5)
</dt> <dt>

**Zugriff verweigert** (6)
</dt> <dt>

**DMTF Reserved** (..)
</dt> <dt>

**Herstellerspezifisch** (32768..65535)
</dt> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1<br/>                                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ ConcreteJob**](cim-concretejob.md)
</dt> </dl>

 

 




