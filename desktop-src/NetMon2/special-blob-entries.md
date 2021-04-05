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
# <a name="special-blob-entries"></a><span data-ttu-id="32f69-103">Spezielle BLOB-Einträge</span><span class="sxs-lookup"><span data-stu-id="32f69-103">Special BLOB Entries</span></span>

<span data-ttu-id="32f69-104">In den folgenden Beispielen wird die [**setstringinblob**](setstringinblob.md) -Funktion verwendet, um spezielle BLOB-Einträge zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="32f69-104">The following examples use the [**SetStringInBlob**](setstringinblob.md) function to create special BLOB entries.</span></span>

## <a name="npp-name"></a><span data-ttu-id="32f69-105">NPP-Name</span><span class="sxs-lookup"><span data-stu-id="32f69-105">NPP Name</span></span>

``` syntax
SetStringInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_LOCATION,
   TAG_NAME,
   "My NPP Name"); 
```

## <a name="npp-class-identifier"></a><span data-ttu-id="32f69-106">NPP-Klassen Bezeichner</span><span class="sxs-lookup"><span data-stu-id="32f69-106">NPP Class Identifier</span></span>

``` syntax
SetClassIDInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_LOCATION,
   TAG_CLASSID,
   &CLSID_ThisNPP);
```

## <a name="cfgproc-procedure-name"></a><span data-ttu-id="32f69-107">Name der cfgproc-Prozedur</span><span class="sxs-lookup"><span data-stu-id="32f69-107">CFGPROC Procedure Name</span></span>

``` syntax
SetStringInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_FINDER,
   TAG_PROCNAME,
   "MyGetNPPBlobs");
```

## <a name="tree-root-name-for-finder-ui"></a><span data-ttu-id="32f69-108">Struktur Stamm Name für die Finder-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="32f69-108">Tree Root Name for Finder UI</span></span>

``` syntax
SetStringInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_FINDER,
   TAG_ROOT,
   "My Tree Root name");
```

## <a name="display-string-for-finder-ui"></a><span data-ttu-id="32f69-109">Anzeige Zeichenfolge für Finder-UI</span><span class="sxs-lookup"><span data-stu-id="32f69-109">Display String for Finder UI</span></span>

``` syntax
SetStringInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_FINDER,
   TAG_DISP_STRING,
   "Double click to select my UI");
```

## <a name="interface-tags"></a><span data-ttu-id="32f69-110">Schnittstellen Tags</span><span class="sxs-lookup"><span data-stu-id="32f69-110">Interface Tags</span></span>

<span data-ttu-id="32f69-111">Dieses Beispiel enthält jede Schnittstelle, die vom NPP unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="32f69-111">This example includes every interface supported by the NPP.</span></span>

``` syntax
SetBoolInBlob(  
   hBlob,
   OWNER_NPP,
   CATEGORY_CONFIG,
   TAG_INTERFACE_REALTIME_CAPTURE,
   TRUE);
```

 

 



