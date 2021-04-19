---
description: Zusätzlich zu dem Zugriff über die IVssBackupComponents-Schnittstelle über das Geräte Objekt der Kopie kann ein Anforderer eine Schatten Kopie für andere Prozesse als ein bereitgestelltes Schreib geschütztes Gerät verfügbar machen.
ms.assetid: 0898c2dc-992a-411b-81df-4f5e129f6a80
title: Verfügbar machen und überwinden von schattenkopierten Volumes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d684aa9b696facaf1caa3aa3102c6b1d7fc37409
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353975"
---
# <a name="exposing-and-surfacing-shadow-copied-volumes"></a><span data-ttu-id="de2fd-103">Verfügbar machen und überwinden von schattenkopierten Volumes</span><span class="sxs-lookup"><span data-stu-id="de2fd-103">Exposing and Surfacing Shadow Copied Volumes</span></span>

<span data-ttu-id="de2fd-104">Zusätzlich zu dem Zugriff über die [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) -Schnittstelle über das [*Geräte Objekt*](vssgloss-d.md)der Kopie kann ein Anforderer eine Schatten Kopie für andere Prozesse als ein bereitgestelltes Schreib geschütztes Gerät verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="de2fd-104">In addition to being accessed through the [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) interface by means of its copy's [*device object*](vssgloss-d.md), a requester can make a shadow copy available to other processes as a mounted read-only device.</span></span>

<span data-ttu-id="de2fd-105">Dieser Prozess wird als verfügbar machen [*einer Schatten Kopie*](vssgloss-e.md)bezeichnet und mithilfe der [**IVssBackupComponents:: exposesnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-exposesnapshot) -Methode ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="de2fd-105">This process is known as [*exposing a shadow copy*](vssgloss-e.md), and is performed using the [**IVssBackupComponents::ExposeSnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-exposesnapshot) method.</span></span>

<span data-ttu-id="de2fd-106">Eine Schatten Kopie kann als lokales Volume verfügbar gemacht werden – ein Laufwerk Buchstabe zugewiesen oder einem bereitgestellten Ordner – oder als Dateifreigabe zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="de2fd-106">A shadow copy can be exposed as a local volume—assigned a drive letter or associated with a mounted folder—or as a file share.</span></span>

<span data-ttu-id="de2fd-107">Um dies zu veranschaulichen, betrachten Sie eine Schatten Kopie, die auf einem Volume auf dem in F: bereitgestellten System exposedsys enthalten ist \\ .</span><span class="sxs-lookup"><span data-stu-id="de2fd-107">To illustrate, consider a shadow copy made of a volume on the system exposedSys mounted at F:\\ on whose root are the directories dirOne and dirTwo, and the file FileOne.</span></span>

## <a name="exposing-a-shadow-copy-locally"></a><span data-ttu-id="de2fd-108">Lokales verfügbar machen einer Schatten Kopie</span><span class="sxs-lookup"><span data-stu-id="de2fd-108">Exposing a Shadow Copy Locally</span></span>

<span data-ttu-id="de2fd-109">Bei der Bereitstellung als lokales Volume wird der Stamm der Schatten Kopie immer am Einfügepunkt (Laufwerk Buchstabe oder eingebundenes Ordner) angezeigt, und alle Dateien mit Schatten Kopie sind sichtbar.</span><span class="sxs-lookup"><span data-stu-id="de2fd-109">When mounted as a local volume, the shadow copy's root is always visible at the mount point (drive letter or mounted folder) and all the shadow-copied files are visible.</span></span>

<span data-ttu-id="de2fd-110">Wenn die Schatten Kopie lokal über den bereitgestellten Ordner C: \\ shadowoff verfügbar gemacht wurde, finden Sie alle Dateien auf dem Datenträger, \\ die zum Zeitpunkt der Bereitstellung von "c: shadowoff" in F: bereitgestellt wurden \\ .</span><span class="sxs-lookup"><span data-stu-id="de2fd-110">If the shadow copy was locally exposed through the mounted folder C:\\ShadowOfF, you would find all files present on disk mounted at F:\\ at the time of the shadow copy available under C:\\ShadowOfF.</span></span> <span data-ttu-id="de2fd-111">Durch die Untersuchung von c: \\ shadowoff werden die beiden Verzeichnisse "dirone" und "dirtwo" und eine Datei ("") unter "c: \\ shadowoff" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="de2fd-111">Examining C:\\ShadowOfF would reveal two directories, dirOne and dirTwo, and one file, fileOne, under C:\\ShadowOfF.</span></span>

<span data-ttu-id="de2fd-112">Ein lokaler Befehl zum verfügbar machen der Schatten Kopie könnte wie folgt lauten:</span><span class="sxs-lookup"><span data-stu-id="de2fd-112">A call to locally expose the shadow copy might be:</span></span>

``` syntax
  IVssBackupComponents *pReq;
  VSS_ID snapID;
  PWSTR wszExposed;
  //    .
  //    .
  hr = pReg->ExposeSnapshot(
         snapID,                           // VSS_ID SnapshotId,
         NULL,                             // VSS_PWSZ wszPathFromRoot
         VSS_VOLSNAP_ATTR_EXPOSED_LOCALLY, // LONG lAttributes
         L"C:\ShadowOfF",                  // VSS_PWSZ wszExpose
         LPWSTR &wszExposed,               // VSS_PWSZ* pwszExposed
       );
```

<span data-ttu-id="de2fd-113">Wenn die Schatten Kopie erfolgreich lokal verfügbar gemacht wurde, sollte *wszexposed* die breit Zeichen-Zeichenfolge "C: \\ shadowoff" enthalten.</span><span class="sxs-lookup"><span data-stu-id="de2fd-113">If the shadow copy was successfully exposed locally, *wszExposed* should contain the wide character string "C:\\ShadowOfF."</span></span>

<span data-ttu-id="de2fd-114">Die Schatten Kopie kann später durch Aufrufen von [**IVssBackupComponentsEx2:: unexposesnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-unexposesnapshot)nicht verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="de2fd-114">The shadow copy can later be unexposed by calling [**IVssBackupComponentsEx2::UnexposeSnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-unexposesnapshot).</span></span>

<span data-ttu-id="de2fd-115">Nur persistente Schatten Kopien – d. h. Schatten Kopien, die entweder mit einem VSS \_ ctx \_ NAS- \_ Rollback oder einem VSS \_ ctx- \_ App-Rollback erstellt wurden \_ – können lokal verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="de2fd-115">Only persistent shadow copies—that is, shadow copies created with either VSS\_CTX\_NAS\_ROLLBACK or VSS\_CTX\_APP\_ROLLBACK—can be exposed locally.</span></span>

## <a name="exposing-a-shadow-copy-as-a-remote-share"></a><span data-ttu-id="de2fd-116">Verfügbar machen einer Schatten Kopie als Remote Freigabe</span><span class="sxs-lookup"><span data-stu-id="de2fd-116">Exposing a Shadow Copy as a Remote Share</span></span>

<span data-ttu-id="de2fd-117">Alternativ dazu können Sie auch festlegen, dass die Schatten Kopie des Datenträgers in F: \\ verfügbar als Remote Dateifreigabe eingebunden werden soll, und dass nur Daten unter dirtwo verfügbar gemacht werden, wenn die Dateifreigabe dirtwooff ist.</span><span class="sxs-lookup"><span data-stu-id="de2fd-117">Alternatively, you could choose to make the shadow copy of the disk mounted at F:\\ available as a remote file share, and expose only data under dirTwo as the file share dirTwoOfF.</span></span>

<span data-ttu-id="de2fd-118">In diesem Fall können Systeme auf die Schatten Kopie von Dateien unter F: \\ dirtwo zugreifen, indem Sie \\ \\ exposedsys \\ dirtwooff als Netzwerklaufwerk Mapping.</span><span class="sxs-lookup"><span data-stu-id="de2fd-118">In this case, systems could access the shadow copy of files under F:\\dirTwo by mapping \\\\exposedSys\\dirTwoOfF as a network drive.</span></span>

<span data-ttu-id="de2fd-119">Ein Befehl zum Implementieren der Remote verfügbar machung der Schatten Kopie als Freigabe könnte wie folgt lauten:</span><span class="sxs-lookup"><span data-stu-id="de2fd-119">A call to implement remote exposing the shadow copy as a share might be the following:</span></span>

``` syntax
  IVssBackupComponents *pReq;
  VSS_ID snapID;
  LPWSTR wszExposed;
  //    .
  //    .
  hr = pReg->ExposeSnapshot(
               snapID,                            // VSS_ID SnapshotId,
               L"\dirTwo",                        // VSS_PWSZ wszPathFromRoot
               VSS_VOLSNAP_ATTR_EXPOSED_REMOTELY, // LONG lAttributes
               L"dirTwoOfF",                      // VSS_PWSZ wszExpose
               LPWSTR &wszExposed,                // VSS_PWSZ* pwszExposed
       );
```

<span data-ttu-id="de2fd-120">Wenn die Schatten Kopie erfolgreich Remote verfügbar gemacht wurde, sollte *wszexposed* die Zeichenfolge "dirtwooff" der breit Zeichenfolge enthalten.</span><span class="sxs-lookup"><span data-stu-id="de2fd-120">If the shadow copy was successfully exposed remotely, *wszExposed* should contain the wide character string "dirTwoOfF."</span></span>

<span data-ttu-id="de2fd-121">Jedes System, das zurzeit die Netzwerkfreigabe von dirtwooff zuordnet, kann die Verbindung mit dem System trennen, genauso wie es von einer normalen Freigabe getrennt werden kann.</span><span class="sxs-lookup"><span data-stu-id="de2fd-121">Any system currently mapping the network share of dirTwoOfF could disconnect from it, just as it might disconnect from any ordinary share.</span></span>

## <a name="surfacing-a-shadow-copy"></a><span data-ttu-id="de2fd-122">Sehen Sie sich eine Schatten Kopie an</span><span class="sxs-lookup"><span data-stu-id="de2fd-122">Surfacing a Shadow Copy</span></span>

<span data-ttu-id="de2fd-123">Eine [*übereinstellungsschattenkopie*](vssgloss-s.md) ist eine, in der die Schatten Kopie dem Mount Manager-Namespace eines Systems bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="de2fd-123">A [*surfaced shadow copy*](vssgloss-s.md) is one in which the shadow copy is known to a system's Mount Manager namespace.</span></span>

<span data-ttu-id="de2fd-124">Dies bedeutet, dass Sie diese Schatten Kopien wie jedes andere verfügbare, aber noch nicht bereitgestellte Volume suchen können – beispielsweise mithilfe von " **findfirstvolume** " und " **findnextvolume**".</span><span class="sxs-lookup"><span data-stu-id="de2fd-124">This means that you can locate such shadow copies just as you would locate any other available but not-yet-mounted volume—by using **FindFirstVolume** and **FindNextVolume**, for example.</span></span>

<span data-ttu-id="de2fd-125">Offensichtlich werden auch Schatten Kopien mit dem verfügbar gemachten Schatten kopiert.</span><span class="sxs-lookup"><span data-stu-id="de2fd-125">Clearly, then, exposed shadow copies are also surfaced shadow copies.</span></span> <span data-ttu-id="de2fd-126">Das Gegenteil ist jedoch nicht unbedingt der Fall.</span><span class="sxs-lookup"><span data-stu-id="de2fd-126">However, the reverse is not necessarily true.</span></span>

<span data-ttu-id="de2fd-127">Wenn die Bereitstellung einer lokal verfügbar gemachten Schatten Kopie aufgehoben wurde oder ein System die Verbindung mit einer Remote zugänglichen Schatten Kopie getrennt hat, wird diese Schatten Kopie nicht mehr verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="de2fd-127">If a locally exposed shadow copy was dismounted, or a system chose to disconnect a remotely exposed shadow copy, that shadow copy would no longer be exposed.</span></span> <span data-ttu-id="de2fd-128">Solange die Schatten Kopie persistent gespeichert wird, werden die Volumes jedoch angezeigt.</span><span class="sxs-lookup"><span data-stu-id="de2fd-128">However, as long as the shadow copy persisted, the volumes would be surfaced.</span></span> <span data-ttu-id="de2fd-129">Dies bedeutet, dass Sie wie jedes andere schreibgeschützte Volume bereitgestellt werden können.</span><span class="sxs-lookup"><span data-stu-id="de2fd-129">This means they could be mounted like any other read-only volume.</span></span>

 

 



