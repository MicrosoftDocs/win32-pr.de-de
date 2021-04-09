---
description: Die dvddirectory-Eigenschaft legt das aktuelle Verzeichnis des aktuellen DVD-Volumes fest oder ruft es ab.
ms.assetid: 0dbfdf28-cda5-41b2-82ce-114d9b940d91
title: Dvddirectory (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36515c931fb8669db814886dfff12a4bf85bde28
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860280"
---
# <a name="dvddirectory-property"></a><span data-ttu-id="a3365-103">Dvddirectory (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="a3365-103">DVDDirectory Property</span></span>

> [!Note]  
> <span data-ttu-id="a3365-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a3365-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="a3365-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="a3365-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="a3365-106">Die- `DVDDirectory` Eigenschaft legt das aktuelle Verzeichnis des aktuellen DVD-Volumes fest oder ruft es ab.</span><span class="sxs-lookup"><span data-stu-id="a3365-106">The `DVDDirectory` property sets or retrieves the current directory of the current DVD volume.</span></span>

``` syntax
[ sDirPath = ] MSWebDVD.DVDDirectory
```

## <a name="return-value"></a><span data-ttu-id="a3365-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a3365-107">Return Value</span></span>

<span data-ttu-id="a3365-108">Gibt einen Zeichen folgen Wert zurück, der den Pfad zum DVD-Stammverzeichnis angibt.</span><span class="sxs-lookup"><span data-stu-id="a3365-108">Returns a string value indicating the path to the DVD root directory.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3365-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a3365-109">Remarks</span></span>

<span data-ttu-id="a3365-110">Diese Eigenschaft ist Lese-/Schreibzugriff und hat keinen Standardwert.</span><span class="sxs-lookup"><span data-stu-id="a3365-110">This property is read/write with no default value.</span></span> <span data-ttu-id="a3365-111">Verwenden Sie diese Methode, um den Stammpfad festzulegen, wenn mehr als ein DVD-Laufwerk auf einem System vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a3365-111">Use this method to set the root path when there is more than one DVD drive on a system.</span></span> <span data-ttu-id="a3365-112">Wenn nur ein Laufwerk auf dem System vorhanden ist und der Laufwerk Buchstabe höher als "C" ist, findet das mswebdvd-Objekt es automatisch.</span><span class="sxs-lookup"><span data-stu-id="a3365-112">When there is only one drive on the system and its drive letter is higher than "C", the MSWebDVD object finds it automatically.</span></span> <span data-ttu-id="a3365-113">Für eine Standard DVD-Video-CD sollte der Stammpfad das TS- \_ Video Verzeichnis enthalten:</span><span class="sxs-lookup"><span data-stu-id="a3365-113">For a standard DVD-Video disc, the root path should include the ts\_video directory:</span></span>


```VB
MSWebDVD.DVDDirectory = "e:\\video_ts"
```



<span data-ttu-id="a3365-114">Einige DVD-Volumes können Ihr Video in einem Verzeichnis mit dem Namen "Video \_ TS" enthalten.</span><span class="sxs-lookup"><span data-stu-id="a3365-114">Some DVD volumes may have their video in a directory named something other than "video\_ts."</span></span> <span data-ttu-id="a3365-115">Die allgemeine Idee ist, dass ein zusätzliches "DVD-Volume" (der Satz von. IFO.</span><span class="sxs-lookup"><span data-stu-id="a3365-115">The general idea is that an additional "DVD volume" (the set of .IFO.</span></span> <span data-ttu-id="a3365-116">VOB und. BUP-Dateien, die normalerweise im Verzeichnis "Video TS" gespeichert werden, \_ können in einem Unterverzeichnis auf der Festplatte abgelegt werden. Wenn Sie den Stamm so ändern, dass er auf dieses Verzeichnis verweist, wird mswebdvd auf diesem separaten DVD-Volume ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a3365-116">VOB, and .BUP files that would normally be stored in the VIDEO\_TS directory) can be placed in a subdirectory on the disc. By changing the root to point to this directory, MSWebDVD will operate on this separate DVD volume.</span></span> <span data-ttu-id="a3365-117">Ein neuer Satz von Menüs, Titeln usw. ist unabhängig von den Titeln im Video TS-Stamm verfügbar, auf \_ die nicht mehr zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="a3365-117">A new set of menus, titles, and so on will be available, independent of the titles in the VIDEO\_TS root, which will no longer be accessible.</span></span> <span data-ttu-id="a3365-118">Solche Verzeichnisse werden als "verborgene Verzeichnisse" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="a3365-118">Such directories are called "hidden directories."</span></span> <span data-ttu-id="a3365-119">Im folgenden Beispiel wird gezeigt, wie ein ausgeblendetes Verzeichnis als Stamm festgelegt wird, wobei "Hidden" ein Platzhalter für den Namen ist, den die Autoren der CD dem Verzeichnis gegeben haben.</span><span class="sxs-lookup"><span data-stu-id="a3365-119">The following example shows how to set a hidden directory as the root, where "hidden" is a placeholder for whatever name the disc authors have given to the directory.</span></span>


```VB
MSWebDVD.DVDDirectory = "d:\\webdvd\\hidden"
```



 

 



