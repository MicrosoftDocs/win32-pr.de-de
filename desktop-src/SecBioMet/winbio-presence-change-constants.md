---
title: WINBIO_PRESENCE_CHANGE Konstanten (winbio \_ types. h)
description: Beschreibt die Arten von Änderungen, die auftreten können, wenn der Windows-Biometrieframework das vorhanden sein von Einzelpersonen überwacht.
ms.assetid: 1E0B65D8-A38F-46BA-A99A-18666729FA30
topic_type:
- apiref
api_name:
- WINBIO_PRESENCE_CHANGE_TYPE_UNKNOWN
- WINBIO_PRESENCE_CHANGE_TYPE_UPDATE_ALL
- WINBIO_PRESENCE_CHANGE_TYPE_ARRIVE
- WINBIO_PRESENCE_CHANGE_TYPE_RECOGNIZE
- WINBIO_PRESENCE_CHANGE_TYPE_DEPART
- WINBIO_PRESENCE_CHANGE_TYPE_TRACK
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2c864c82ddca6faec134716778dc2e795675371
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040208"
---
# <a name="winbio_presence_change-constants"></a><span data-ttu-id="e5026-103">Winbio- \_ Anwesenheits \_ Änderungs Konstanten</span><span class="sxs-lookup"><span data-stu-id="e5026-103">WINBIO\_PRESENCE\_CHANGE Constants</span></span>

<span data-ttu-id="e5026-104">Beschreibt die Arten von Änderungen, die auftreten können, wenn der Windows-Biometrieframework das vorhanden sein von Einzelpersonen überwacht.</span><span class="sxs-lookup"><span data-stu-id="e5026-104">Describes the types of changes that can occur when the Windows Biometric Framework monitors the presence of individuals.</span></span>



| <span data-ttu-id="e5026-105">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="e5026-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                      | <span data-ttu-id="e5026-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e5026-106">Description</span></span>                                                                                                                                               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_UNKNOWN"></span><span id="winbio_presence_change_type_unknown"></span><dl> <span data-ttu-id="e5026-107"><dt>**Winbio \_ Anwesenheits \_ \_ Änderungstyp \_ unbekannt**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e5026-107"><dt>**WINBIO\_PRESENCE\_CHANGE\_TYPE\_UNKNOWN**</dt> <dt>0</dt></span></span> </dl>           | <span data-ttu-id="e5026-108">Der Ereignistyp ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="e5026-108">The type of event is unknown.</span></span> <span data-ttu-id="e5026-109">Dieser Wert wird für die nicht initialisierte Struktur verwendet.</span><span class="sxs-lookup"><span data-stu-id="e5026-109">This value is used for the uninitialized structure.</span></span><br/>                                                              |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_UPDATE_ALL"></span><span id="winbio_presence_change_type_update_all"></span><dl> <span data-ttu-id="e5026-110"><dt>**Winbio \_ Anwesenheits \_ \_ Änderungstyp \_ Update \_ alle**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e5026-110"><dt>**WINBIO\_PRESENCE\_CHANGE\_TYPE\_UPDATE\_ALL**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="e5026-111">Enthält Informationen zu allen Gesichtern, die im Kamera Rahmen aktuell sind.</span><span class="sxs-lookup"><span data-stu-id="e5026-111">Provides information about all of the faces current in the camera frame.</span></span><br/>                                                                       |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_ARRIVE"></span><span id="winbio_presence_change_type_arrive"></span><dl> <span data-ttu-id="e5026-112"><dt>**Winbio \_ Anwesenheits \_ \_ Änderungstyp \_ Ankunft**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e5026-112"><dt>**WINBIO\_PRESENCE\_CHANGE\_TYPE\_ARRIVE**</dt> <dt>2</dt></span></span> </dl>              | <span data-ttu-id="e5026-113">Ein neues Gesicht, das in den Kamera Rahmen gelangt.</span><span class="sxs-lookup"><span data-stu-id="e5026-113">A new face entered the camera frame.</span></span><br/>                                                                                                           |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_RECOGNIZE"></span><span id="winbio_presence_change_type_recognize"></span><dl> <span data-ttu-id="e5026-114"><dt>**Winbio \_ Anwesenheits \_ \_ Änderungstyp \_ erkennen**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e5026-114"><dt>**WINBIO\_PRESENCE\_CHANGE\_TYPE\_RECOGNIZE**</dt> <dt>3</dt></span></span> </dl>     | <span data-ttu-id="e5026-115">Es wurde ein Gesicht mit einem registrierten Benutzer abgeglichen.</span><span class="sxs-lookup"><span data-stu-id="e5026-115">A face was matched to an enrolled user.</span></span><br/>                                                                                                        |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_DEPART"></span><span id="winbio_presence_change_type_depart"></span><dl> <span data-ttu-id="e5026-116"><dt>**Winbio \_ Anwesenheits \_ \_ Änderungstyp \_**</dt> <dt>4</dt> .</span><span class="sxs-lookup"><span data-stu-id="e5026-116"><dt>**WINBIO\_PRESENCE\_CHANGE\_TYPE\_DEPART**</dt> <dt>4</dt></span></span> </dl>              | <span data-ttu-id="e5026-117">Ein zuvor erkanntes Gesicht befand sich seit einem bestimmten Zeitraum nicht mehr im Kamera Frame.</span><span class="sxs-lookup"><span data-stu-id="e5026-117">A previously detected face has been out of the camera frame for a period of time.</span></span><br/>                                                              |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_TRACK"></span><span id="winbio_presence_change_type_track"></span><dl> <span data-ttu-id="e5026-118"><dt>**Winbio \_ Anwesenheits \_ \_ Änderungstyp nach \_ Verfolgung**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="e5026-118"><dt>**WINBIO\_PRESENCE\_CHANGE\_TYPE\_TRACK**</dt> <dt>5</dt></span></span> </dl>                 | <span data-ttu-id="e5026-119">Stellt Update Informationen über das umgebende Feld bereit und gibt Detail Werte für eine Teilmenge der Gesichter zurück, die sich derzeit im Kamera Rahmen befinden.</span><span class="sxs-lookup"><span data-stu-id="e5026-119">Provides updates information about the bounding box and reject detail values for a subset of the faces that are currently in the camera frame.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="e5026-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e5026-120">Requirements</span></span>



| <span data-ttu-id="e5026-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e5026-121">Requirement</span></span> | <span data-ttu-id="e5026-122">Wert</span><span class="sxs-lookup"><span data-stu-id="e5026-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5026-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e5026-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e5026-124">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e5026-124">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="e5026-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e5026-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e5026-126">Nur Windows Server 2016 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e5026-126">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="e5026-127">Header</span><span class="sxs-lookup"><span data-stu-id="e5026-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5026-128"><dt>Winbio \_ types. h (Include winbio. h für Client Anwendungen oder winbio \_ Adapters. h für Adapter)</dt></span><span class="sxs-lookup"><span data-stu-id="e5026-128"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



 

 





