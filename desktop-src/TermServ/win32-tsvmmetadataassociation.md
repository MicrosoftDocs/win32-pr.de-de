---
title: Win32_TSVmMetadataAssociation-Klasse
description: Stellt eine Zuordnung zwischen einem virtuellen Remotedesktop und dessen Metadateneigenschaften dar.
ms.assetid: 374b1a29-78de-45fd-97b3-c5a5b724e66b
ms.tgt_platform: multiple
keywords:
- Win32_TSVmMetadataAssociation-Remotedesktopdienste
- Win32_TSVmMetadataAssociation klasse Remotedesktopdienste , beschrieben
topic_type:
- apiref
api_name:
- Win32_TSVmMetadataAssociation
- Win32_TSVmMetadataAssociation.TSVm
- Win32_TSVmMetadataAssociation.MetadataItem
api_location:
- TSVmHostWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebe3389bb03c9e3f33a2cc3e33450318b68171f7ac35fffeaaa3976cb5ae3a33
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119420000"
---
# <a name="win32_tsvmmetadataassociation-class"></a>Win32 \_ TSVmMetadataAssociation-Klasse

Stellt eine Zuordnung zwischen einem virtuellen Remotedesktop und dessen Metadateneigenschaften dar.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[dynamic, Association, provider("Win32_TSVmHost_Prov"), AMENDMENT]
class Win32_TSVmMetadataAssociation
{
  Win32_TSVm             REF TSVm;
  Win32_TSVmMetadataItem REF MetadataItem;
};
```

## <a name="members"></a>Member

Die **Win32 \_ TSVmMetadataAssociation-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ TSVmMetadataAssociation-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Metadataitem**
</dt> <dd> <dl> <dt>

Datentyp: **[ **Win32 \_ TSVmMetadataItem**](win32-tsvmmetadataitem.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Instanz der [**Win32 \_ TSVmMetadataItem-Klasse,**](win32-tsvmmetadataitem.md) die die Metadaten für den virtuellen Computer darstellt.

</dd> <dt>

**TSVm**
</dt> <dd> <dl> <dt>

Datentyp: **[ **Win32 \_ TSVm**](win32-tsvm.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Eine Instanz der [**Win32 \_ TSVm-Klasse,**](win32-tsvm.md) die den virtuellen Computer darstellt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                             |
| Namespace<br/>                | Root \\ CIMV2 \\ TerminalServices<br/>                                                   |
| MOF<br/>                      | <dl> <dt>TSVmHost.mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TSVmHostWmi.dll</dt> </dl> |



 

