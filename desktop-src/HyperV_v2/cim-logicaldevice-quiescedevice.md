---
description: Die QuiesceDevice-Methode ist anstelle der allgemeineren RequestStateChange-Methode veraltet, die sich direkt mit der von dieser Methode bereitgestellten Funktionalität überschneidet.
ms.assetid: c5154c00-ff9c-40d8-bb76-41ae72ce86ae
title: QuiesceDevice-Methode der CIM_LogicalDevice-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.QuiesceDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c7becb86f19c245488d779e1b26ab5321ba3f2aa0ac3c7811d96f9d1cb8a5dbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117995692"
---
# <a name="quiescedevice-method-of-the-cim_logicaldevice-class"></a>QuiesceDevice-Methode der CIM \_ LogicalDevice-Klasse

Die **QuiesceDevice-Methode** ist anstelle der allgemeineren **RequestStateChange-Methode** veraltet, die sich direkt mit der von dieser Methode bereitgestellten Funktionalität überschneidet.

## <a name="syntax"></a>Syntax


```mof
uint32 QuiesceDevice(
  [in] boolean Quiesce
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Stille Klammer* \[ In\]
</dt> <dd>

Wenn diese Einstellung auf **TRUE** festgelegt ist, beenden Sie alle Aktivitäten sauber, wenn **FALSE** die Aktivität fortsetzen soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg den Wert 0 zurück. andernfalls wird ein Fehler zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1<br/>                                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Root-Virtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CIM \_ LogicalDevice**](cim-logicaldevice.md)
</dt> </dl>

 

 




