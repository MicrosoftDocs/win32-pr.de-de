---
description: Die Aufruf Methode der CIM \_ removefileaction-Klasse führt eine bestimmte Aktion aus. Die Details, wie die Methode die Aktion ausführt, sind Implementierungs spezifisch. Diese Methode wird von der CIM- \_ Aktion geerbt.
ms.assetid: 7fc33654-a51b-41cf-a5b4-ef08fd6e40ac
ms.tgt_platform: multiple
title: Aufruf Methode der CIM_RemoveFileAction-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RemoveFileAction.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a371ad1f7b1da874b6a049b04d5f50ec694cf181
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344950"
---
# <a name="invoke-method-of-the-cim_removefileaction-class"></a>Aufruf Methode der CIM \_ removefileaction-Klasse

Die **Aufruf** Methode der [**CIM \_ removefileaction**](cim-removefileaction.md) -Klasse führt eine bestimmte Aktion aus. Die Details, wie die Methode die Aktion ausführt, sind Implementierungs spezifisch. Diese Methode wird von der [**CIM- \_ Aktion**](cim-action.md)geerbt.

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

[CIM- \_ removefileaction](invoke-method-in-class-cim-removefileaction.md)
</dt> <dt>

[**CIM- \_ removefileaction**](cim-removefileaction.md)
</dt> </dl>

 

