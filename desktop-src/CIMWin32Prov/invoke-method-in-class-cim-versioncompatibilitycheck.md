---
description: Die Aufruf Methode der CIM \_ versioncompatibilitycheck-Klasse wertet eine bestimmte Überprüfung aus.
ms.assetid: d1ccc248-340e-4277-9696-063e1e2bf915
ms.tgt_platform: multiple
title: Aufruf Methode der CIM_VersionCompatibilityCheck-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VersionCompatibilityCheck.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: bccbb6072ae84a238b60247daf6b81cfaa74e608
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860928"
---
# <a name="invoke-method-of-the-cim_versioncompatibilitycheck-class"></a>Aufruf Methode der CIM \_ versioncompatibilitycheck-Klasse

Die **Aufruf** Methode der [**CIM \_ versioncompatibilitycheck**](cim-versioncompatibilitycheck.md) -Klasse wertet eine bestimmte Überprüfung aus. Die Details, wie die Methode eine bestimmte Überprüfung in einem CIM-Kontext auswertet, werden von den nicht abstrakten [**CIM- \_ Check**](cim-check.md) -Unterklassen beschrieben. Diese Methode wird von der **CIM- \_ Überprüfung** geerbt.

> [!IMPORTANT]
> Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).

 

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntax


```mof
uint32 Invoke();
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

[CIM \_ versioncompatibilitycheck](invoke-method-in-class-cim-versioncompatibilitycheck.md)
</dt> <dt>

[**CIM \_ versioncompatibilitycheck**](cim-versioncompatibilitycheck.md)
</dt> </dl>

 

