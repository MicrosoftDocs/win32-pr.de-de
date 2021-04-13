---
title: Mrmpackagingmode-Enumeration (mrmresourcindexer. h)
description: Definiert Konstanten, die angeben, welche Art von PRI-Dateien von mrmkreateresourcefile und mrmkreateresourcefileinmemory erstellt werden sollen.
ms.assetid: 5695B67E-5446-4538-83D2-F8FF91A5080E
keywords:
- Mrmpackagingmode-enumerationsmenüs und andere Ressourcen
topic_type:
- apiref
api_name:
- MrmPackagingMode
api_location:
- MrmResourceIndexer.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eaca681dbcf9d171e279083abbb730895ff99333
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340738"
---
# <a name="mrmpackagingmode-enumeration"></a>Mrmpackagingmode-Enumeration

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Definiert Konstanten, die angeben, welche Art von PRI-Dateien von [**mrmkreateresourcefile**](mrmcreateresourcefile.md) und [**mrmkreateresourcefileinmemory**](mrmcreateresourcefileinmemory.md)erstellt werden sollen. Weitere Informationen und szenariobasierte Exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter API für [Paket Ressourcen Indizierung (PRI) und benutzerdefinierte Buildsysteme](/windows/uwp/app-resources/pri-apis-custom-build-systems).

## <a name="syntax"></a>Syntax


```C++
typedef enum _MrmPackagingMode { 
  MrmPackagingModeStandaloneFile  = 0,
  MrmPackagingModeAutoSplit       = 1,
  MrmPackagingModeResourcePack    = 2
} MrmPackagingMode;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="MrmPackagingModeStandaloneFile"></span><span id="mrmpackagingmodestandalonefile"></span><span id="MRMPACKAGINGMODESTANDALONEFILE"></span>**Mrmpackagingmodestandalonefile**
</dt> <dd>

Gibt an, dass eine einzelne PRI-Datei erstellt werden soll.

</dd> <dt>

<span id="MrmPackagingModeAutoSplit"></span><span id="mrmpackagingmodeautosplit"></span><span id="MRMPACKAGINGMODEAUTOSPLIT"></span>**Mrmpackagingmodeautosplit**
</dt> <dd>

Gibt an, dass mehrere PRI-Dateien erstellt werden sollen. automatisch von allen unterstützten Qualifizierern (insbesondere Sprache und Skalierung) aufteilen.

</dd> <dt>

<span id="MrmPackagingModeResourcePack"></span><span id="mrmpackagingmoderesourcepack"></span><span id="MRMPACKAGINGMODERESOURCEPACK"></span>**Mrmpackagingmoderesourcepack**
</dt> <dd>

Gibt an, dass eine Add-on-Satelliten-PRI-Datei erstellt werden soll.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1803, \[ nur Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ -Desktop-Apps\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>Mrmresourceingedexer. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[APIs für die Paketressourcenindizierung (PRI) und benutzerdefinierte Buildsysteme](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

