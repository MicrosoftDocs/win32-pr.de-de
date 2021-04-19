---
title: Win32_TSVmMetadataAssociation-Klasse
description: Stellt eine Zuordnung zwischen einer Remotedesktop virtuellen Maschine und ihren Metadateneigenschaften dar.
ms.assetid: 374b1a29-78de-45fd-97b3-c5a5b724e66b
ms.tgt_platform: multiple
keywords:
- Win32_TSVmMetadataAssociation-Klasse Remotedesktopdienste
- Win32_TSVmMetadataAssociation Klasse Remotedesktopdienste, beschrieben
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
ms.openlocfilehash: db3a68c20553eaf52903471d19df9df169ecde21
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341586"
---
# <a name="win32_tsvmmetadataassociation-class"></a>Win32- \_ TSVmMetadataAssociation-Klasse

Stellt eine Zuordnung zwischen einer Remotedesktop virtuellen Maschine und ihren Metadateneigenschaften dar.

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

Die **Win32- \_ TSVmMetadataAssociation** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32- \_ TSVmMetadataAssociation** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**MetadataItem**
</dt> <dd> <dl> <dt>

Datentyp: **[ **Win32 \_ TSVmMetadataItem**](win32-tsvmmetadataitem.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Instanz der [**Win32- \_ TSVmMetadataItem**](win32-tsvmmetadataitem.md) -Klasse, die die Metadaten für den virtuellen Computer darstellt.

</dd> <dt>

**Out-VM**
</dt> <dd> <dl> <dt>

Datentyp: **[ **Win32- \_ VM**](win32-tsvm.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Eine Instanz der Win32-Klasse " [**\_ ZVM**](win32-tsvm.md) ", die den virtuellen Computer darstellt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                             |
| Namespace<br/>                | Root \\ CIMV2 \\ TerminalServices<br/>                                                   |
| MOF<br/>                      | <dl> <dt>"Zvmhost. mof"</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TSVmHostWmi.dll</dt> </dl> |



 

