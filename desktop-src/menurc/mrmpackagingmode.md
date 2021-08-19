---
title: MrmPackagingMode-Enumeration (MrmResourceIndexer.h)
description: Definiert Konstanten, die angeben, welche Art von PRI-Datei(en) von MrmCreateResourceFile und MrmCreateResourceFileInMemory erstellt werden soll.
ms.assetid: 5695B67E-5446-4538-83D2-F8FF91A5080E
keywords:
- MrmPackagingMode-Enumerationsmenüs und andere Ressourcen
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
ms.openlocfilehash: 58b4e968a43ba08786cc433b199bef5c07431420ac5942646530960279ea853e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117870149"
---
# <a name="mrmpackagingmode-enumeration"></a>MrmPackagingMode-Enumeration

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Definiert Konstanten, die angeben, welche Art von PRI-Datei(en) von [**MrmCreateResourceFile**](mrmcreateresourcefile.md) und [**MrmCreateResourceFileInMemory erstellt werden soll.**](mrmcreateresourcefileinmemory.md) Weitere Informationen und szenariobasierte exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter APIs für die Paketressourcenindizierung und benutzerdefinierte [Buildsysteme.](/windows/uwp/app-resources/pri-apis-custom-build-systems)

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

<span id="MrmPackagingModeStandaloneFile"></span><span id="mrmpackagingmodestandalonefile"></span><span id="MRMPACKAGINGMODESTANDALONEFILE"></span>**MrmPackagingModeStandaloneFile**
</dt> <dd>

Gibt an, dass eine einzelne PRI-Datei erstellt werden soll.

</dd> <dt>

<span id="MrmPackagingModeAutoSplit"></span><span id="mrmpackagingmodeautosplit"></span><span id="MRMPACKAGINGMODEAUTOSPLIT"></span>**MrmPackagingModeAutoSplit**
</dt> <dd>

Gibt an, dass mehrere PRI-Dateien erstellt werden sollen. Automatisches Aufteilen nach allen unterstützten Qualifizierern (insbesondere Sprache und Skalierung).

</dd> <dt>

<span id="MrmPackagingModeResourcePack"></span><span id="mrmpackagingmoderesourcepack"></span><span id="MRMPACKAGINGMODERESOURCEPACK"></span>**MrmPackagingModeResourcePack**
</dt> <dd>

Gibt an, dass eine Add-On-Satelliten-PRI-Datei erstellt werden soll.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, version 1803 desktop apps only (Nur \[ Desktop-Apps der Version 1803)\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur \[ Serverdesktop-Apps\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>MrmResourceIndexer.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[APIs für die Paketressourcenindizierung (PRI) und benutzerdefinierte Buildsysteme](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

