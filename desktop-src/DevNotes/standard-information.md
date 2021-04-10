---
description: Enthält das Standard Informations Attribut. Dieses Attribut ist in jedem Basisdatei Daten Satz vorhanden und muss ansässig sein.
ms.assetid: 8e668309-2722-4115-923d-bf0aa78d24f1
title: STANDARD_INFORMATION Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STANDARD_INFORMATION
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4927553ac593475f8659932468227362ae19fe59
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041321"
---
# <a name="standard_information-structure"></a>Standard \_ Informationsstruktur

\[Diese Struktur gilt nur für Version 3 von NTFS-Volumes. Sie kann in zukünftigen Versionen geändert werden.\]

Enthält das Standard Informations Attribut. Dieses Attribut ist in jedem Basisdatei Daten Satz vorhanden und muss ansässig sein.

## <a name="syntax"></a>Syntax


```C++
typedef struct _STANDARD_INFORMATION {
  UCHAR Reserved[0x30];
  ULONG OwnerId;
  ULONG SecurityId;
} STANDARD_INFORMATION, *PSTANDARD_INFORMATION;
```



## <a name="members"></a>Member

<dl> <dt>

**Reserved**
</dt> <dd>

Reserviert.

</dd> <dt>

**OwnerID**
</dt> <dd>

Der Bezeichner des Datei Besitzers aus dem Sicherheitsindex.

</dd> <dt>

**Securityid**
</dt> <dd>

Die Sicherheits-ID für die Datei.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Beachten Sie, dass es für diese Struktur keine zugeordnete Header Datei gibt.

Diese Struktur Definition ist nur für die Hauptversion 3 und die neben Version 0 oder 1 gültig, wie von [**FSCTL \_ get \_ NTFS \_ Volume \_ Data**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data)berichtet.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Master Dateitabelle](master-file-table.md)
</dt> </dl>

 

 
