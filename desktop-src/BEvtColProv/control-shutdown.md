---
description: Beendet den Collector. Wenn der Collector als Dienst ausgeführt wird, ist das Beenden des Diensts der bessere Ansatz.
ms.assetid: fab3e060-156f-46f5-98a2-d47a23d64552
ms.tgt_platform: multiple
title: Shutdown-Methode der Control-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.Shutdown
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 6a83b798ff89116ad0e7cadad1a4dac74b3722bdbb2410c1cad09a3ac8c9c710
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529660"
---
# <a name="shutdown-method-of-the-control-class"></a>Shutdown-Methode der Control-Klasse

Beendet den Collector. Wenn der Collector als Dienst ausgeführt wird, ist das Beenden des Diensts der bessere Ansatz.

## <a name="syntax"></a>Syntax


```mof
void Shutdown();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                       |
| Namespace<br/>                | Root \\ Microsoft \\ Windows \\ BootEventCollector<br/>                                              |
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Control**](control.md)
</dt> </dl>

 

 




