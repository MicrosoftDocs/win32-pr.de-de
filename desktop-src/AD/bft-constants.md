---
title: Bft-Konstanten (ntdsbcli. h)
description: Die bft-Konstanten werden als Bitflags verwendet, um unterschiedliche Dateitypen in einer Active Directory Domain Services Sicherung zu identifizieren.
ms.assetid: 3658a657-d9e3-4fbf-9120-4b0205b81a36
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- BFT_LOG_DIRECTORY
- BFT_DATABASE_DIRECTORY
- BFT_DIRECTORY
- BFT_LOG
- BFT_LOG_DIR
- BFT_CHECKPOINT_DIR
- BFT_NTDS_DATABASE
- BFT_PATCH_FILE
- BFT_UNKNOWN
api_location:
- Ntdsbcli.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9607b5e61e5689d8895b39a11aa7e813fc7fcbe6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949722"
---
# <a name="bft-constants"></a><span data-ttu-id="f835b-103">Bft-Konstanten</span><span class="sxs-lookup"><span data-stu-id="f835b-103">BFT Constants</span></span>

<span data-ttu-id="f835b-104">Die bft-Konstanten werden als Bitflags verwendet, um unterschiedliche Dateitypen in einer Active Directory Domain Services Sicherung zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="f835b-104">The BFT constants are used as bit flags to identify different file types in an Active Directory Domain Services backup.</span></span>

<dl> <dt>

<span data-ttu-id="f835b-105"><span id="BFT_LOG_DIRECTORY"></span><span id="bft_log_directory"></span>**bft- \_ Protokoll \_ Verzeichnis**</span><span class="sxs-lookup"><span data-stu-id="f835b-105"><span id="BFT_LOG_DIRECTORY"></span><span id="bft_log_directory"></span>**BFT\_LOG\_DIRECTORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f835b-106">0x20</span><span class="sxs-lookup"><span data-stu-id="f835b-106">0x20</span></span>
</dt> <dt>



<span data-ttu-id="f835b-107">Die Datei gehört zum Protokoll Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="f835b-107">The file belongs in the log directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f835b-108"><span id="BFT_DATABASE_DIRECTORY"></span><span id="bft_database_directory"></span>**bft- \_ Daten Bank \_ Verzeichnis**</span><span class="sxs-lookup"><span data-stu-id="f835b-108"><span id="BFT_DATABASE_DIRECTORY"></span><span id="bft_database_directory"></span>**BFT\_DATABASE\_DIRECTORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f835b-109">0x40</span><span class="sxs-lookup"><span data-stu-id="f835b-109">0x40</span></span>
</dt> <dt>



<span data-ttu-id="f835b-110">Die Datei gehört zum Datenbankverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="f835b-110">The file belongs in the database directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f835b-111"><span id="BFT_DIRECTORY"></span><span id="bft_directory"></span>**bft- \_ Verzeichnis**</span><span class="sxs-lookup"><span data-stu-id="f835b-111"><span id="BFT_DIRECTORY"></span><span id="bft_directory"></span>**BFT\_DIRECTORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f835b-112">0x80</span><span class="sxs-lookup"><span data-stu-id="f835b-112">0x80</span></span>
</dt> <dt>



<span data-ttu-id="f835b-113">Der angegebene Pfad ist ein Verzeichnis und kein Dateiname.</span><span class="sxs-lookup"><span data-stu-id="f835b-113">The path specified is a directory and not a file name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f835b-114"><span id="BFT_LOG"></span><span id="bft_log"></span>**bft- \_ Protokoll**</span><span class="sxs-lookup"><span data-stu-id="f835b-114"><span id="BFT_LOG"></span><span id="bft_log"></span>**BFT\_LOG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f835b-115">0x21</span><span class="sxs-lookup"><span data-stu-id="f835b-115">0x21</span></span>
</dt> <dt>



<span data-ttu-id="f835b-116">Gibt eine Protokolldatei an, die zum Protokoll Verzeichnis gehört.</span><span class="sxs-lookup"><span data-stu-id="f835b-116">Specifies a log file that belongs in the log directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f835b-117"><span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>**bft- \_ Protokoll Verzeichnis \_**</span><span class="sxs-lookup"><span data-stu-id="f835b-117"><span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>**BFT\_LOG\_DIR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f835b-118">0x22</span><span class="sxs-lookup"><span data-stu-id="f835b-118">0x22</span></span>
</dt> <dt>



<span data-ttu-id="f835b-119">Die Datei ist der Pfad des Protokoll Verzeichnisses.</span><span class="sxs-lookup"><span data-stu-id="f835b-119">The file is the path of the log directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f835b-120"><span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>**bft-Prüf Punkt Verzeichnis \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f835b-120"><span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>**BFT\_CHECKPOINT\_DIR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f835b-121">0x23</span><span class="sxs-lookup"><span data-stu-id="f835b-121">0x23</span></span>
</dt> <dt>



<span data-ttu-id="f835b-122">Die Datei ist der Pfad des Checkpoint-Verzeichnisses.</span><span class="sxs-lookup"><span data-stu-id="f835b-122">The file is the path of the checkpoint directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f835b-123"><span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**bft- \_ NTDS- \_ Datenbank**</span><span class="sxs-lookup"><span data-stu-id="f835b-123"><span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**BFT\_NTDS\_DATABASE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f835b-124">0x44</span><span class="sxs-lookup"><span data-stu-id="f835b-124">0x44</span></span>
</dt> <dt>



<span data-ttu-id="f835b-125">Bei der Datei handelt es sich um eine Verzeichnisdienst-Datenbank, die im Datenbankverzeichnis gehört.</span><span class="sxs-lookup"><span data-stu-id="f835b-125">The file is a directory service database that belongs in the database directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f835b-126"><span id="BFT_PATCH_FILE"></span><span id="bft_patch_file"></span>**bft \_ - \_ Patchdatei**</span><span class="sxs-lookup"><span data-stu-id="f835b-126"><span id="BFT_PATCH_FILE"></span><span id="bft_patch_file"></span>**BFT\_PATCH\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f835b-127">0x25</span><span class="sxs-lookup"><span data-stu-id="f835b-127">0x25</span></span>
</dt> <dt>



<span data-ttu-id="f835b-128">Bei der Datei handelt es sich um eine Patchdatei, die zum Protokoll Verzeichnis gehört.</span><span class="sxs-lookup"><span data-stu-id="f835b-128">The file is a patch file that belongs in the log directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f835b-129"><span id="BFT_UNKNOWN"></span><span id="bft_unknown"></span>**bft \_ unbekannt**</span><span class="sxs-lookup"><span data-stu-id="f835b-129"><span id="BFT_UNKNOWN"></span><span id="bft_unknown"></span>**BFT\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f835b-130">0x0f</span><span class="sxs-lookup"><span data-stu-id="f835b-130">0x0F</span></span>
</dt> <dt>



<span data-ttu-id="f835b-131">Die Datei kann nicht erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="f835b-131">The file cannot be recognized.</span></span> <span data-ttu-id="f835b-132">Die Datei stimmt nicht mit den bekannten Dateinamen und Dateitypen überein.</span><span class="sxs-lookup"><span data-stu-id="f835b-132">The file does not coincide with the known file names and file types.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f835b-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f835b-133">Requirements</span></span>



| <span data-ttu-id="f835b-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f835b-134">Requirement</span></span> | <span data-ttu-id="f835b-135">Wert</span><span class="sxs-lookup"><span data-stu-id="f835b-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f835b-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f835b-136">Minimum supported client</span></span><br/> | <span data-ttu-id="f835b-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f835b-137">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="f835b-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f835b-138">Minimum supported server</span></span><br/> | <span data-ttu-id="f835b-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f835b-139">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="f835b-140">Header</span><span class="sxs-lookup"><span data-stu-id="f835b-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="f835b-141"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="f835b-141"><dt>Ntdsbcli.h</dt></span></span> </dl> |



 

 





