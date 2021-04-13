---
title: Plug-in-Strukturen
description: Strukturen für die Entwicklung von Client Anwendungen durch die Windows-Biometrieframework-API.
ms.assetid: 64fb908c-72c2-4639-a2f6-77ede080512c
keywords:
- Windows-Biometrieframework API-Windows-Biometrieframework-API, Plug-in-Strukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 193b5a99f30c76e8e6e2ab7ebf0242cf56905816
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310876"
---
# <a name="plug-in-structures"></a><span data-ttu-id="9550b-104">Plug-in-Strukturen</span><span class="sxs-lookup"><span data-stu-id="9550b-104">Plug-in Structures</span></span>

<span data-ttu-id="9550b-105">Die folgenden Strukturen werden für die Entwicklung von Client Anwendungen durch die Windows-Biometrieframework-API unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9550b-105">The following structures are supported for client application development by the Windows Biometric Framework API.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9550b-106">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="9550b-106">In this section</span></span>



| <span data-ttu-id="9550b-107">Thema</span><span class="sxs-lookup"><span data-stu-id="9550b-107">Topic</span></span>                                                                                                | <span data-ttu-id="9550b-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9550b-108">Description</span></span>                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9550b-109">**winbio- \_ Konto \_ Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="9550b-109">**WINBIO\_ACCOUNT\_POLICY**</span></span>](winbio-account-policy.md)<br/>                                  | <span data-ttu-id="9550b-110">Enthält entweder eine Standard-oder eine kontospezifische Antispoofing-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="9550b-110">Contains either a default or account-specific antispoofing policy.</span></span><br/>                                                         |
| [<span data-ttu-id="9550b-111">**winbio \_ Adapter \_ Interface- \_ Version**</span><span class="sxs-lookup"><span data-stu-id="9550b-111">**WINBIO\_ADAPTER\_INTERFACE\_VERSION**</span></span>](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_adapter_interface_version)<br/>           | <span data-ttu-id="9550b-112">Enthält eine Haupt-und neben Versionsnummer, die in den Tabellen-, Sensor-und Speicher Adapter-Schnittstellen Tabellen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9550b-112">Contains a major and minor version number used in the engine, sensor, and storage adapter interface tables.</span></span><br/>                |
| [<span data-ttu-id="9550b-113">**winbio- \_ Engine- \_ Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="9550b-113">**WINBIO\_ENGINE\_INTERFACE**</span></span>](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_engine_interface)<br/>                              | <span data-ttu-id="9550b-114">Enthält Zeiger auf die benutzerdefinierten Engine-Adapter Funktionen.</span><span class="sxs-lookup"><span data-stu-id="9550b-114">Contains pointers to your custom engine adapter functions.</span></span><br/>                                                                 |
| [<span data-ttu-id="9550b-115">**Erweiterte winbio-Registrierungs \_ \_ \_ Parameter**</span><span class="sxs-lookup"><span data-stu-id="9550b-115">**WINBIO\_EXTENDED\_ENROLLMENT\_PARAMETERS**</span></span>](winbio-extended-enrollment-parameters.md)<br/> | <span data-ttu-id="9550b-116">Enthält zusätzliche Informationen, die ein Engine-Adapter zum Erstellen einer Registrierungs Vorlage benötigt.</span><span class="sxs-lookup"><span data-stu-id="9550b-116">Contains additional information that an engine adapter needs to create an enrollment template.</span></span> <br/>                            |
| [<span data-ttu-id="9550b-117">**winbio- \_ Pipeline**</span><span class="sxs-lookup"><span data-stu-id="9550b-117">**WINBIO\_PIPELINE**</span></span>](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_pipeline)<br/>                                               | <span data-ttu-id="9550b-118">Enthält freigegebene Kontextinformationen, die von den Sensor-, Engine-und Speicher Adapter Komponenten in einer einzelnen biometrischen Einheit verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9550b-118">Contains shared context information used by the sensor, engine, and storage adapter components in a single biometric unit.</span></span><br/> |
| [<span data-ttu-id="9550b-119">**winbio- \_ Sensor \_ Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="9550b-119">**WINBIO\_SENSOR\_INTERFACE**</span></span>](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_sensor_interface)<br/>                              | <span data-ttu-id="9550b-120">Enthält Zeiger auf die benutzerdefinierten Sensor Adapter Funktionen.</span><span class="sxs-lookup"><span data-stu-id="9550b-120">Contains pointers to your custom sensor adapter functions.</span></span><br/>                                                                 |
| [<span data-ttu-id="9550b-121">**winbio- \_ Speicher \_ Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="9550b-121">**WINBIO\_STORAGE\_INTERFACE**</span></span>](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_storage_interface)<br/>                            | <span data-ttu-id="9550b-122">Enthält Zeiger auf die benutzerdefinierten Speicher Adapter Funktionen.</span><span class="sxs-lookup"><span data-stu-id="9550b-122">Contains pointers to your custom storage adapter functions.</span></span><br/>                                                                |
| [<span data-ttu-id="9550b-123">**winbio- \_ Speicher \_ Daten Satz**</span><span class="sxs-lookup"><span data-stu-id="9550b-123">**WINBIO\_STORAGE\_RECORD**</span></span>](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_storage_record)<br/>                                  | <span data-ttu-id="9550b-124">Enthält eine biometrische Vorlage und zugehörige Daten in einem Standardformat.</span><span class="sxs-lookup"><span data-stu-id="9550b-124">Contains a biometric template and associated data in a standard format.</span></span><br/>                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="9550b-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9550b-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9550b-126">Plug-in-Referenz</span><span class="sxs-lookup"><span data-stu-id="9550b-126">Plug-in Reference</span></span>](plug-in-reference.md)
</dt> <dt>

[<span data-ttu-id="9550b-127">Plug-in-Funktionen</span><span class="sxs-lookup"><span data-stu-id="9550b-127">Plug-in Functions</span></span>](plug-in-functions.md)
</dt> <dt>

[<span data-ttu-id="9550b-128">**Wbioqueryengineinterface**</span><span class="sxs-lookup"><span data-stu-id="9550b-128">**WbioQueryEngineInterface**</span></span>](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioqueryengineinterface)
</dt> <dt>

[<span data-ttu-id="9550b-129">**Wbioquerysensorinterface**</span><span class="sxs-lookup"><span data-stu-id="9550b-129">**WbioQuerySensorInterface**</span></span>](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioquerysensorinterface)
</dt> <dt>

[<span data-ttu-id="9550b-130">**Wbioquerystorageinterface**</span><span class="sxs-lookup"><span data-stu-id="9550b-130">**WbioQueryStorageInterface**</span></span>](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioquerystorageinterface)
</dt> </dl>

 

 





