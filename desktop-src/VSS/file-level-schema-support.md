---
description: Writer können die Leistung verschiedener Sicherungs Typen auf Datei Satz Ebene optimieren, indem Sie den Sicherungstyp für die Datei Angabe angeben, der durch eine Bitmaske oder bitweise OR der Member der VSS- \_ dateispezifizierungstyp- \_ \_ \_ Enumeration angegeben wird.
ms.assetid: a3ac69b4-894a-4536-8fab-f45ad7e5118a
title: Schema Unterstützung auf Dateiebene
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 460d256a3eaa016933e697687d05e26838c14ae2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960735"
---
# <a name="file-level-schema-support"></a><span data-ttu-id="86c08-103">Schema Unterstützung auf Dateiebene</span><span class="sxs-lookup"><span data-stu-id="86c08-103">File Level Schema Support</span></span>

<span data-ttu-id="86c08-104">Writer können die Leistung verschiedener Sicherungs Typen auf [*Datei Satz*](vssgloss-f.md) Ebene optimieren, indem Sie den Sicherungstyp für die Datei Angabe angeben, der durch eine Bitmaske oder bitweise OR der Member der [**VSS- \_ dateispezifizierungstyp \_ \_ \_**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) -Enumeration angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="86c08-104">Writers can fine-tune the performance of various types of backup at the [*file set*](vssgloss-f.md) level by indicating through a file specification backup type, indicated by a bit mask or bitwise OR of the members of the [**VSS\_FILE\_SPEC\_BACKUP\_TYPE**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) enumeration.</span></span>

<span data-ttu-id="86c08-105">Für angegebene Sicherungs Typen gibt der Writer Folgendes an:</span><span class="sxs-lookup"><span data-stu-id="86c08-105">For specified types of backup, the writer indicates the following:</span></span>

-   <span data-ttu-id="86c08-106">Gibt an, ob es erforderlich ist, das Volume mit einem Schatten zu kopieren, um einen Datei Satz ordnungsgemäß zu sichern.</span><span class="sxs-lookup"><span data-stu-id="86c08-106">Whether it will be necessary to shadow copy the volume to properly back up a file set.</span></span> <span data-ttu-id="86c08-107">Wenn beispielsweise die Dateien in einem Datei Satz nicht exklusiv vom Writer geöffnet werden und sichergestellt werden können, dass Sie stabil sind, wird keine Schatten Kopie benötigt.</span><span class="sxs-lookup"><span data-stu-id="86c08-107">For instance, if the files in a file set are not exclusively opened by the writer and it can ensure that it is stable, a shadow copy is not needed.</span></span>
-   <span data-ttu-id="86c08-108">Gibt an, ob der Anforderer die Sicherung so ausführen muss, dass unabhängig vom Zeitpunkt der letzten Änderung oder anderen Problemen die bei der Sicherung aktuelle Version der Dateien des Datei Satzes wieder hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="86c08-108">Whether the requester has to perform the backup in such a way that, regardless of last modification time or other issues, the version of the file set's files current at backup will be restored.</span></span> <span data-ttu-id="86c08-109">In der Regel bedeutet dies, dass der Dateisatz als Teil der Sicherung kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="86c08-109">Typically, this means that the file set is copied as part of the backup.</span></span>

<span data-ttu-id="86c08-110">Die Werte für den [**Sicherungstyp der VSS-Datei Spezifikation, die die \_ schattenkopieanforderung \_ \_ \_**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) angeben,</span><span class="sxs-lookup"><span data-stu-id="86c08-110">The values of [**VSS\_FILE\_SPEC\_BACKUP\_TYPE**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) that indicate shadow copy requirement are:</span></span>

-   <span data-ttu-id="86c08-111">VSS \_ fsbt \_ alle \_ Momentaufnahmen \_ erforderlich</span><span class="sxs-lookup"><span data-stu-id="86c08-111">VSS\_FSBT\_ALL\_SNAPSHOT\_REQUIRED</span></span>
-   <span data-ttu-id="86c08-112">Vollständige VSS- \_ fsbt- \_ \_ Momentaufnahme \_ erforderlich</span><span class="sxs-lookup"><span data-stu-id="86c08-112">VSS\_FSBT\_FULL\_SNAPSHOT\_REQUIRED</span></span>
-   <span data-ttu-id="86c08-113">VSS- \_ fsbt- \_ differenzielle \_ Momentaufnahme \_ erforderlich</span><span class="sxs-lookup"><span data-stu-id="86c08-113">VSS\_FSBT\_DIFFERENTIAL\_SNAPSHOT\_REQUIRED</span></span>
-   <span data-ttu-id="86c08-114">VSS \_ fsbt- \_ inkrementelle \_ Momentaufnahme \_ erforderlich</span><span class="sxs-lookup"><span data-stu-id="86c08-114">VSS\_FSBT\_INCREMENTAL\_SNAPSHOT\_REQUIRED</span></span>
-   <span data-ttu-id="86c08-115">VSS- \_ fsbt- \_ Protokoll \_ Momentaufnahme \_ erforderlich</span><span class="sxs-lookup"><span data-stu-id="86c08-115">VSS\_FSBT\_LOG\_SNAPSHOT\_REQUIRED</span></span>

<span data-ttu-id="86c08-116">Die Werte für den [**\_ \_ \_ \_ Sicherungstyp der VSS-Datei Spezifikation**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) , die die Anforderung zum Sichern einer Datei angeben, lauten:</span><span class="sxs-lookup"><span data-stu-id="86c08-116">The values of [**VSS\_FILE\_SPEC\_BACKUP\_TYPE**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) that indicate the requirement to back up a file are:</span></span>

-   <span data-ttu-id="86c08-117">VSS \_ fsbt \_ alle \_ Sicherungen \_ erforderlich</span><span class="sxs-lookup"><span data-stu-id="86c08-117">VSS\_FSBT\_ALL\_BACKUP\_REQUIRED</span></span>
-   <span data-ttu-id="86c08-118">Vollständige VSS- \_ fsbt- \_ \_ Sicherung \_ erforderlich</span><span class="sxs-lookup"><span data-stu-id="86c08-118">VSS\_FSBT\_FULL\_BACKUP\_REQUIRED</span></span>
-   <span data-ttu-id="86c08-119">VSS- \_ fsbt- \_ differenzielle \_ Sicherung \_ erforderlich</span><span class="sxs-lookup"><span data-stu-id="86c08-119">VSS\_FSBT\_DIFFERENTIAL\_BACKUP\_REQUIRED</span></span>
-   <span data-ttu-id="86c08-120">\_ \_ inkrementelle Sicherung von VSS fsbt \_ \_ erforderlich</span><span class="sxs-lookup"><span data-stu-id="86c08-120">VSS\_FSBT\_INCREMENTAL\_BACKUP\_REQUIRED</span></span>
-   <span data-ttu-id="86c08-121">VSS- \_ fsbt- \_ Protokoll \_ Sicherung \_ erforderlich</span><span class="sxs-lookup"><span data-stu-id="86c08-121">VSS\_FSBT\_LOG\_BACKUP\_REQUIRED</span></span>

<span data-ttu-id="86c08-122">Standardmäßig werden Dateigruppen mit dem Sicherungstyp "Datei Spezifikation" VSS \_ fsbt \_ alle \_ Sicherungen \_ erforderlich \| VSS \_ fsbt \_ alle \_ Momentaufnahmen \_ erforderlich. Dies bedeutet, dass bei der Verarbeitung der Datei Satz Dateien immer eine Schatten Kopie erforderlich ist und dass die Dateien in alle Sicherungs Typen kopiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="86c08-122">By default, file sets are tagged with a file specification backup type of VSS\_FSBT\_ALL\_BACKUP\_REQUIRED \| VSS\_FSBT\_ALL\_SNAPSHOT\_REQUIRED, meaning that a shadow copy is always required in handling the file set's files, and that the files should be copied in all types of backup.</span></span>

 

 



