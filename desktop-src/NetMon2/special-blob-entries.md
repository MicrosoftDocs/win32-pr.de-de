---
description: In den folgenden Beispielen wird die SetStringInBlob-Funktion verwendet, um spezielle BLOB-Einträge zu erstellen.
ms.assetid: 4a921b0d-9934-48e2-8837-be0bd7b7fa7a
title: Spezielle BLOB-Einträge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0659fa05219dcc715c6c00b3d28635e2500f73e4e5bece72049ee43839a0820
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118363138"
---
# <a name="special-blob-entries"></a>Spezielle BLOB-Einträge

In den folgenden Beispielen wird die [**SetStringInBlob-Funktion**](setstringinblob.md) verwendet, um spezielle BLOB-Einträge zu erstellen.

## <a name="npp-name"></a>NPP-Name

``` syntax
SetStringInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_LOCATION,
   TAG_NAME,
   "My NPP Name"); 
```

## <a name="npp-class-identifier"></a>NPP-Klassenbezeichner

``` syntax
SetClassIDInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_LOCATION,
   TAG_CLASSID,
   &CLSID_ThisNPP);
```

## <a name="cfgproc-procedure-name"></a>CFGPROC-Prozedurname

``` syntax
SetStringInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_FINDER,
   TAG_PROCNAME,
   "MyGetNPPBlobs");
```

## <a name="tree-root-name-for-finder-ui"></a>Strukturstammname für die Finder-Benutzeroberfläche

``` syntax
SetStringInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_FINDER,
   TAG_ROOT,
   "My Tree Root name");
```

## <a name="display-string-for-finder-ui"></a>Anzeigen einer Zeichenfolge für die Finder-Benutzeroberfläche

``` syntax
SetStringInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_FINDER,
   TAG_DISP_STRING,
   "Double click to select my UI");
```

## <a name="interface-tags"></a>Schnittstellentags

Dieses Beispiel enthält jede schnittstelle, die vom NPP unterstützt wird.

``` syntax
SetBoolInBlob(  
   hBlob,
   OWNER_NPP,
   CATEGORY_CONFIG,
   TAG_INTERFACE_REALTIME_CAPTURE,
   TRUE);
```

 

 



