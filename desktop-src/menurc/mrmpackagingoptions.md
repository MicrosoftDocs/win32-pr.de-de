---
title: MrmPackagingOptions-Enumeration (MrmResourceIndexer.h)
description: Definiert Konstanten, die Optionen für die PRI-Datei angeben, die von MrmCreateResourceFile und MrmCreateResourceFileInMemory erstellt wurde.
ms.assetid: 11FADCB2-CE6F-449E-8A85-DA50B52B26D0
keywords:
- MrmPackagingOptions-Enumerationsmenüs und andere Ressourcen
topic_type:
- apiref
api_name:
- MrmPackagingOptions
api_location:
- MrmResourceIndexer.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ede8ef1367bc217827f616514a4fb9ea69e180cb654a19cbbe9593d4c74036d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971969"
---
# <a name="mrmpackagingoptions-enumeration"></a>MrmPackagingOptions-Enumeration

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Definiert Konstanten, die Optionen für die PRI-Datei angeben, die von [**MrmCreateResourceFile**](mrmcreateresourcefile.md) und [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md)erstellt wurde. Weitere Informationen und szenariobasierte exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter APIs für [die Paketressourcenindizierung (PACKAGE Resource Indexing, PRI) und benutzerdefinierte Buildsysteme.](/windows/uwp/app-resources/pri-apis-custom-build-systems)

## <a name="syntax"></a>Syntax


```C++
typedef enum _MrmPackagingOptions { 
  MrmPackagingOptionsNone                         = 0x00,
  MrmPackagingOptionsOmitSchemaFromResourcePacks  = 0x01,
  MrmPackagingOptionsSplitLanguageVariants        = 0x02
} MrmPackagingOptions;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="MrmPackagingOptionsNone"></span><span id="mrmpackagingoptionsnone"></span><span id="MRMPACKAGINGOPTIONSNONE"></span>**MrmPackagingOptionsNone**
</dt> <dd>

Gibt keine Paketierungsoptionen an.

</dd> <dt>

<span id="MrmPackagingOptionsOmitSchemaFromResourcePacks"></span><span id="mrmpackagingoptionsomitschemafromresourcepacks"></span><span id="MRMPACKAGINGOPTIONSOMITSCHEMAFROMRESOURCEPACKS"></span>**MrmPackagingOptionsOmitSchemaFromResourcePacks**
</dt> <dd>

Gibt an, dass ein schemafreies Ressourcenpaket erstellt werden soll.

</dd> <dt>

<span id="MrmPackagingOptionsSplitLanguageVariants"></span><span id="mrmpackagingoptionssplitlanguagevariants"></span><span id="MRMPACKAGINGOPTIONSSPLITLANGUAGEVARIANTS"></span>**MrmPackagingOptionsSplitLanguageVariants**
</dt> <dd>

Gibt an, dass die PRI-Datei automatisch von allen unterstützten Qualifizierern (insbesondere Sprache und Skalierung) aufgeteilt werden soll.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, nur Desktop-Apps der Version 1803 \[\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Windows \[Nur Serverdesktop-Apps\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>MrmResourceIndexer.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[APIs für die Paketressourcenindizierung (PRI) und benutzerdefinierte Buildsysteme](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

