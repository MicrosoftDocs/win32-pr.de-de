---
description: Network DDE stellt Funktionen bereit, mit denen Sie eine Freigabe löschen, Freigabe Informationen erhalten oder festlegen oder Freigaben aufzählen können.
ms.assetid: d7924e93-75e4-4f94-b159-02408535170d
title: Verwalten von DDE Shares
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fcc8c7d2eb3983aaabd054b9b729daea176bb10
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "104350949"
---
# <a name="managing-dde-shares"></a><span data-ttu-id="56512-103">Verwalten von DDE Shares</span><span class="sxs-lookup"><span data-stu-id="56512-103">Managing DDE Shares</span></span>

<span data-ttu-id="56512-104">\[Network DDE wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="56512-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="56512-105">Nddeapi.dll ist unter Windows Vista vorhanden, aber alle Funktionsaufrufe geben "ndde" \_ nicht \_ implementiert zurück.\]</span><span class="sxs-lookup"><span data-stu-id="56512-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="56512-106">Network DDE stellt Funktionen bereit, mit denen Sie eine Freigabe löschen, Freigabe Informationen erhalten oder festlegen oder Freigaben aufzählen können.</span><span class="sxs-lookup"><span data-stu-id="56512-106">Network DDE provides functions that allow you to delete a share, get or set share information, or enumerate shares.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="56512-107">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="56512-107">Task</span></span></th>
<th><span data-ttu-id="56512-108">Prozedur</span><span class="sxs-lookup"><span data-stu-id="56512-108">Procedure</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="56512-109">Löschen einer DDE-Freigabe</span><span class="sxs-lookup"><span data-stu-id="56512-109">Delete a DDE share</span></span></td>
<td><span data-ttu-id="56512-110">Verwenden Sie die <a href="nddesharedel.md"><strong>nddebug</strong></a> -Funktion.</span><span class="sxs-lookup"><span data-stu-id="56512-110">Use the <a href="nddesharedel.md"><strong>NDdeShareDel</strong></a> function.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="56512-111">Informationen zur DDE-Freigabe erhalten</span><span class="sxs-lookup"><span data-stu-id="56512-111">Get DDE share information</span></span></td>
<td><span data-ttu-id="56512-112">Verwenden Sie die <a href="nddesharegetinfo.md"><strong>ndde sharegetinfo</strong></a> -Funktion.</span><span class="sxs-lookup"><span data-stu-id="56512-112">Use the <a href="nddesharegetinfo.md"><strong>NDdeShareGetInfo</strong></a> function.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="56512-113">Festlegen der DDE-Freigabe Informationen</span><span class="sxs-lookup"><span data-stu-id="56512-113">Set DDE share information</span></span></td>
<td><span data-ttu-id="56512-114">Verwenden Sie die <a href="nddesharesetinfo.md"><strong>nddesharesetinfo</strong></a> -Funktion.</span><span class="sxs-lookup"><span data-stu-id="56512-114">Use the <a href="nddesharesetinfo.md"><strong>NDdeShareSetInfo</strong></a> function.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="56512-115">DDE-Freigaben aufzählen</span><span class="sxs-lookup"><span data-stu-id="56512-115">Enumerate DDE shares</span></span></td>
<td><span data-ttu-id="56512-116">Verwenden Sie die <a href="nddeshareenum.md"><strong>ndde ShareEnum</strong></a> -Funktion.</span><span class="sxs-lookup"><span data-stu-id="56512-116">Use the <a href="nddeshareenum.md"><strong>NDdeShareEnum</strong></a> function.</span></span> <span data-ttu-id="56512-117">Sie können auch die vertrauenswürdigen DDE-Freigaben mithilfe der <a href="nddetrustedshareenum.md"><strong>nddebug</strong></a> -Funktion auflisten.</span><span class="sxs-lookup"><span data-stu-id="56512-117">You can also enumerate the trusted DDE shares by using the <a href="nddetrustedshareenum.md"><strong>NDdeTrustedShareEnum</strong></a> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="56512-118">Auflisten verbundener Benutzer</span><span class="sxs-lookup"><span data-stu-id="56512-118">Enumerate connected users</span></span></td>
<td><span data-ttu-id="56512-119">Verwenden Sie die Funktion " <a href="/windows/desktop/api/lmshare/nf-lmshare-netsessionenum"><strong>netzessionenum</strong></a> ".</span><span class="sxs-lookup"><span data-stu-id="56512-119">Use the <a href="/windows/desktop/api/lmshare/nf-lmshare-netsessionenum"><strong>NetSessionEnum</strong></a> function.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="56512-120">Ändern des DDE-Freigabe namens</span><span class="sxs-lookup"><span data-stu-id="56512-120">Change the DDE share name</span></span></td>
<td><span data-ttu-id="56512-121">Löschen Sie die alte Freigabe, und erstellen Sie eine neue Freigabe.</span><span class="sxs-lookup"><span data-stu-id="56512-121">Delete the old share and create a new share.</span></span>
<ol>
<li><span data-ttu-id="56512-122">Rufen Sie die Freigabe Informationen mit <a href="nddesharegetinfo.md"><strong>nddesharegetinfo</strong></a>ab.</span><span class="sxs-lookup"><span data-stu-id="56512-122">Retrieve the share information using <a href="nddesharegetinfo.md"><strong>NDdeShareGetInfo</strong></a>.</span></span></li>
<li><span data-ttu-id="56512-123">Entfernen Sie die Freigabe mit <a href="nddesharedel.md"><strong>ndabsharedel</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="56512-123">Remove the share using <a href="nddesharedel.md"><strong>NDdeShareDel</strong></a>.</span></span></li>
<li><span data-ttu-id="56512-124">Ändern Sie den <strong>lpszsharename</strong> -Member der <a href="nddeshareinfo-str.md"><strong>ndbeshareinfo</strong></a> -Struktur, die von <a href="nddesharegetinfo.md"><strong>ndbesharegetinfo</strong></a>zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="56512-124">Change the <strong>lpszShareName</strong> member of the <a href="nddeshareinfo-str.md"><strong>NDDESHAREINFO</strong></a> structure returned by <a href="nddesharegetinfo.md"><strong>NDdeShareGetInfo</strong></a>.</span></span></li>
<li><span data-ttu-id="56512-125">Übergeben Sie die geänderte <a href="nddeshareinfo-str.md"><strong>ndbeshareingefo</strong></a> -Struktur an <a href="nddeshareadd.md"><strong>ndabshareadd</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="56512-125">Pass the modified <a href="nddeshareinfo-str.md"><strong>NDDESHAREINFO</strong></a> structure to <a href="nddeshareadd.md"><strong>NDdeShareAdd</strong></a>.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

 

