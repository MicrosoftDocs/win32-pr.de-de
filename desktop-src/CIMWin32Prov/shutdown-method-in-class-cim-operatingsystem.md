---
description: Die Methode zum Herunterfahren fordert das Herunterfahren des Betriebssystems an.
ms.assetid: f2a2a98b-2f4f-4aa1-9f54-515660273c8d
ms.tgt_platform: multiple
title: Shutdown-Methode der CIM_OperatingSystem-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_OperatingSystem.Shutdown
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 78a11f325b8682b0024ff281a48989b837d3073a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860636"
---
# <a name="shutdown-method-of-the-cim_operatingsystem-class"></a>Shutdown-Methode der CIM \_ OperatingSystem-Klasse

Die Methode zum **herunter** fahren fordert das Herunterfahren des Betriebssystems an. Die Implementierung oder Unterklasse des Betriebssystems kann Abhängigkeiten zwischen den Methoden zum **herunter** fahren und [**Neustarten**](reboot-method-in-class-cim-operatingsystem.md) herstellen. Beispielsweise können anspruchsvollere Funktionen bereitgestellt werden, z. b. ein geplantes Herunterfahren und ein Neustart.

> [!IMPORTANT]
> Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).

 

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntax


```mof
uint32 Shutdown();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg den Wert 0 (null) zurück, und jede andere Zahl gibt einen Fehler an.

## <a name="remarks"></a>Bemerkungen

Diese Methode wird zurzeit nicht von WMI implementiert. Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.

Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet. Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[CIM- \_ OperatingSystem](shutdown-method-in-class-cim-operatingsystem.md)
</dt> <dt>

[**CIM- \_ OperatingSystem**](cim-operatingsystem.md)
</dt> </dl>

 

