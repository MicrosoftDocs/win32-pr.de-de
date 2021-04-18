---
title: Platzhalter Dateien
description: Platzhalter Dateien
ms.assetid: E14655DA-CEA0-4106-B882-C9E9116FC234
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93c15037b0daec7a6521a299b6c4587c956e0be3
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "106337270"
---
# <a name="placeholder-files"></a><span data-ttu-id="ee8ac-103">Platzhalter Dateien</span><span class="sxs-lookup"><span data-stu-id="ee8ac-103">Placeholder files</span></span>

## <a name="platform"></a><span data-ttu-id="ee8ac-104">Plattform</span><span class="sxs-lookup"><span data-stu-id="ee8ac-104">Platform</span></span>

<span data-ttu-id="ee8ac-105">**Clients:** Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="ee8ac-105">**Clients -** Windows 8.1</span></span>  
<span data-ttu-id="ee8ac-106">**Server:** Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="ee8ac-106">**Servers -** Windows Server 2012 R2</span></span>  

## <a name="description"></a><span data-ttu-id="ee8ac-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ee8ac-107">Description</span></span>

<span data-ttu-id="ee8ac-108">Platzhalter Dateien ermöglichen es Benutzern, Microsoft onedrive-Dateien unabhängig von der Konnektivität anzuzeigen und zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="ee8ac-108">Placeholder files enable users to view and manage Microsoft OneDrive files regardless of connectivity.</span></span> <span data-ttu-id="ee8ac-109">Platzhalter Dateien stellen den onedrive-Namespace dar, auch wenn Dateien nicht lokal zwischengespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="ee8ac-109">Placeholder files represent the OneDrive namespace, even when files are not cached locally.</span></span> <span data-ttu-id="ee8ac-110">Sie enthalten Datei Metadaten und Miniaturbilder von Fotos.</span><span class="sxs-lookup"><span data-stu-id="ee8ac-110">They contain file metadata and thumbnail images of photos.</span></span>

## <a name="manifestation"></a><span data-ttu-id="ee8ac-111">Ausstrahlung</span><span class="sxs-lookup"><span data-stu-id="ee8ac-111">Manifestation</span></span>

<span data-ttu-id="ee8ac-112">Für Endbenutzer und Entwickler Verhalten sich Platzhalter Dateien fast identisch mit den lokalen Dateien.</span><span class="sxs-lookup"><span data-stu-id="ee8ac-112">To end users and developers, placeholder files look and behave almost the same as the local files.</span></span>

<span data-ttu-id="ee8ac-113">Wenn Ihre APP das Dateisystem mit dem allgemeinen Datei Dialogfeld aufzählt, wird Ihre APP nicht beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="ee8ac-113">If your app uses the Common File Dialog to enumerate the file system, your app will not be impacted.</span></span> <span data-ttu-id="ee8ac-114">Wenn der Benutzer versucht, die Datei im allgemeinen/File-Dialog Feld zu öffnen, wird der Inhalt der Datei heruntergeladen und an Ihre APP übermittelt.</span><span class="sxs-lookup"><span data-stu-id="ee8ac-114">When the user tries to open the file from the common /file Dialog, the file content will be downloaded and will be passed to your app.</span></span>

<span data-ttu-id="ee8ac-115">Wenn Ihre APP direkt auf das Dateisystem zugreift, kann Ihre APP die Platzhalter Dateien mithilfe der unten aufgeführten Richtlinien nutzen.</span><span class="sxs-lookup"><span data-stu-id="ee8ac-115">If your app accesses the file system directly, then your app may take advantage of the placeholder files by using the guidelines below.</span></span>

## <a name="solution"></a><span data-ttu-id="ee8ac-116">Lösung</span><span class="sxs-lookup"><span data-stu-id="ee8ac-116">Solution</span></span>

-   <span data-ttu-id="ee8ac-117">Platzhalter werden auf der Grundlage von Attributen ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="ee8ac-117">Placeholders are hidden by convention based on attributes</span></span>
-   <span data-ttu-id="ee8ac-118">Identifizieren von Platzhaltern mithilfe der Analyse-Tag-ID e/a- \_ \_ \_ Datei \_ Platzhalter</span><span class="sxs-lookup"><span data-stu-id="ee8ac-118">Identify placeholders using reparse tag ID IO\_REPARSE\_TAG\_FILE\_PLACEHOLDER</span></span>

<span data-ttu-id="ee8ac-119">Verwenden Sie das Shell-Datenmodell für nahtloses Verhalten:</span><span class="sxs-lookup"><span data-stu-id="ee8ac-119">Use the shell data model for seamless behavior:</span></span>

-   <span data-ttu-id="ee8ac-120">Verwenden Sie shkreateitemfromparametename () zum Erstellen eines shellelements.</span><span class="sxs-lookup"><span data-stu-id="ee8ac-120">Use SHCreateItemFromParsingName() to create a shell item</span></span>
-   <span data-ttu-id="ee8ac-121">Binden an den Datenstrom mithilfe von IShellItem:: bindtohandler (bhid- \_ Stream)</span><span class="sxs-lookup"><span data-stu-id="ee8ac-121">Bind to the stream using IShellItem::BindToHandler(BHID\_Stream)</span></span>
-   <span data-ttu-id="ee8ac-122">Benutzereigenschaften Handler für den Eigenschaften Zugriff (IShellItem2:: getpropertyhandler)</span><span class="sxs-lookup"><span data-stu-id="ee8ac-122">User property handler for property access (IShellItem2::GetPropertyHandler)</span></span>
-   <span data-ttu-id="ee8ac-123">Benutzershellfingernailhandler zum Aufrufen von Miniaturbildern für Platzhalter</span><span class="sxs-lookup"><span data-stu-id="ee8ac-123">User shell thumbnailhandler to get thumbnail images for placeholders</span></span>
-   <span data-ttu-id="ee8ac-124">Geben Sie supportedprotokolls = \* für Ihre Verb-Implementierung an, wenn das Verb über bindtohandler an den Stream gebunden wird.</span><span class="sxs-lookup"><span data-stu-id="ee8ac-124">Specify SupportedProtocols=\* on your verb implementation if the verb binds to the stream via BindToHandler</span></span>


```
#include <winnth> //for IO_REPARSE_TAG_FILE_PLACEHOLDER
//  Helper that indicates this is a 
bool IsFilePlaceholder(WIN32_FIND_DATA const &findData)
{
  return (findData.dwFileAttributes & FILE_ATTRIBUTE_REPARSE_POINT) &&
    (findData.dwReserved0 == IO_REPARSE_TAG_FILE_PLACEHOLDER);
}
bool IsFilePlaceholder(_In_PCWSTR filePath)
{
  bool isPlaceholder = false;
  WIN32_FIND_DATA findData;
  HANDLE hFind = FindFirstFile(filePath, &findData);
  if (hFind ! = INVALID_HANDLE_VALUE)
  {
    isPlaceholder = (findData.dwFileAttributes &    FILE_ATTRIBUTE_REPARSE_POINT) &&
    (findData.dwReserved0 == IO_REPARSE_TAG_FILE_PLACEHOLDER);
    FindClose(hFind);
  }
  Return isPlaceholder;
}
```



 

 




