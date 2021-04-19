---
description: Überprüft, ob das Rack, auf das verwiesen wird, in das physische Paket eingefügt oder darin eingefügt werden kann.
ms.assetid: 03276c6a-ca48-48bc-adbe-e53e02107abb
ms.tgt_platform: multiple
title: Iscompatible-Methode der CIM_Rack-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Rack.IsCompatible
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6855b797e8941882aac1dc25d77b2ef7e3bc11c1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346438"
---
# <a name="iscompatible-method-of-the-cim_rack-class"></a>Iscompatible-Methode der CIM- \_ Rack-Klasse

Die **iscompatible** -Methode überprüft, ob das Rack, auf das verwiesen wird, in das physische Paket eingefügt oder darin eingefügt werden kann. In einer Unterklasse kann der Satz möglicher Rückgabecodes mit einem **ValueMap** -Qualifizierer für die-Methode angegeben werden. Die Zeichen folgen, in die der **ValueMap** -Inhalt übersetzt wird, können auch in der Unterklasse als **Werte** Array Qualifizierer angegeben werden. Diese Methode wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.

> [!IMPORTANT]
> Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).

 

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntax


```mof
uint32 IsCompatible(
  [in] CIM_PhysicalElement ElementToCheck
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Elementto-Check* \[ in\]
</dt> <dd>

Verweis auf das physische Element, für das diese Methode ausgeführt wird.

</dd> </dl>

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

[**CIM- \_ Rack**](iscompatible-method-in-class-cim-rack.md)
</dt> <dt>

[**CIM- \_ Rack**](cim-rack.md)
</dt> </dl>

 

