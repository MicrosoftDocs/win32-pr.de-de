---
description: Stellt ein Paket mit vier aufrufen dar.
MS-HAID: vspixengine.PackedCallPkg
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Packedcallpkg-Struktur
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: BE345C1A-9F6E-4FE0-99C7-6B332A1ED079
api_name:
- PackedCallPkg
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 104e764725213f7030c90a0240641c7c9b063785
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103957876"
---
# <a name="span-idvspixenginepackedcallpkgspanpackedcallpkg-structure"></a><span id="vspixengine.packedcallpkg"></span>Packedcallpkg-Struktur

Stellt ein Paket mit vier aufrufen dar.

## <a name="syntax"></a>Syntax


```C++
typedef struct PackedCallPkg {
  UINT pcp1;
  UINT pcp2;
  UINT pcp3;
  UINT pcp4;
} PackedCallPkg;
```

## <a name="members"></a>Member

**pcp1**  
Der erste aufzurufende Paket.

**pcp2**  
Der zweite-Befehl im Paket.

**pcp3**  
Der dritte aufzurufende Paket.

**pcp4**  
Der vierte-Befehl im Paket.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



