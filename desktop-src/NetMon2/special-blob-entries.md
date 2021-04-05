---
description: In den folgenden Beispielen wird die setstringinblob-Funktion verwendet, um spezielle BLOB-Einträge zu erstellen.
ms.assetid: 4a921b0d-9934-48e2-8837-be0bd7b7fa7a
title: Spezielle BLOB-Einträge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cfc40029e0a0f88c2f7bd242881b0d750a5dfa1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752176"
---
# <a name="special-blob-entries"></a>Spezielle BLOB-Einträge

In den folgenden Beispielen wird die [**setstringinblob**](setstringinblob.md) -Funktion verwendet, um spezielle BLOB-Einträge zu erstellen.

## <a name="npp-name"></a>NPP-Name

``` syntax
SetStringInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_LOCATION,
   TAG_NAME,
   "My NPP Name"); 
```

## <a name="npp-class-identifier"></a>NPP-Klassen Bezeichner

``` syntax
SetClassIDInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_LOCATION,
   TAG_CLASSID,
   &CLSID_ThisNPP);
```

## <a name="cfgproc-procedure-name"></a>Name der cfgproc-Prozedur

``` syntax
SetStringInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_FINDER,
   TAG_PROCNAME,
   "MyGetNPPBlobs");
```

## <a name="tree-root-name-for-finder-ui"></a>Struktur Stamm Name für die Finder-Benutzeroberfläche

``` syntax
SetStringInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_FINDER,
   TAG_ROOT,
   "My Tree Root name");
```

## <a name="display-string-for-finder-ui"></a>Anzeige Zeichenfolge für Finder-UI

``` syntax
SetStringInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_FINDER,
   TAG_DISP_STRING,
   "Double click to select my UI");
```

## <a name="interface-tags"></a>Schnittstellen Tags

Dieses Beispiel enthält jede Schnittstelle, die vom NPP unterstützt wird.

``` syntax
SetBoolInBlob(  
   hBlob,
   OWNER_NPP,
   CATEGORY_CONFIG,
   TAG_INTERFACE_REALTIME_CAPTURE,
   TRUE);
```

 

 



