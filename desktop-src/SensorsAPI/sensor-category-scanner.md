---
description: In der \_ \_ Kategorie Scanner Kategorie Scanner sind Sensoren enthalten, die Informationen bereitstellen, die durch Scannen abgerufen werden.
ms.assetid: 98a772c9-2a21-489f-ad8d-3b772b7ff892
title: SENSOR_CATEGORY_SCANNER (Sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b38fdb3358ff3ce2ae96ce901972cc6842a0d1b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958820"
---
# <a name="sensor_category_scanner"></a><span data-ttu-id="54966-103">Sensor \_ \_ kategoriescanner</span><span class="sxs-lookup"><span data-stu-id="54966-103">SENSOR\_CATEGORY\_SCANNER</span></span>

<span data-ttu-id="54966-104">In der \_ \_ Kategorie Scanner Kategorie Scanner sind Sensoren enthalten, die Informationen bereitstellen, die durch Scannen abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="54966-104">The SENSOR\_CATEGORY\_SCANNER category contains sensors that provide information that is obtained by scanning.</span></span>

<span data-ttu-id="54966-105">**Platt Form definierte Sensor Typen**</span><span class="sxs-lookup"><span data-stu-id="54966-105">**Platform-Defined Sensor Types**</span></span>

<span data-ttu-id="54966-106">Diese Kategorie enthält die folgenden Platt Form definierten Sensortypen.</span><span class="sxs-lookup"><span data-stu-id="54966-106">This category includes the following platform-defined sensor types.</span></span>



| <span data-ttu-id="54966-107">Sensortyp</span><span class="sxs-lookup"><span data-stu-id="54966-107">Sensor type</span></span>                                                                                                                                                                                                                                                                                           | <span data-ttu-id="54966-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="54966-108">Description</span></span>                                                     |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------|
| <span id="SENSOR_TYPE_BARCODE_SCANNER"></span><span id="sensor_type_barcode_scanner"></span><dl> <span data-ttu-id="54966-109"><dt>**Sensor \_ Geben Sie \_ Barcode \_ Scanner**</dt> <dt>{990b3d8f-85bb-45ff-914d-998c04f372df}</dt> ein.</span><span class="sxs-lookup"><span data-stu-id="54966-109"><dt>**SENSOR\_TYPE\_BARCODE\_SCANNER**</dt> <dt>{990B3D8F-85BB-45FF-914D-998C04F372DF}</dt></span></span> </dl> | <span data-ttu-id="54966-110">Sensoren, die die optische Überprüfung verwenden, um Barcode Codes zu lesen.</span><span class="sxs-lookup"><span data-stu-id="54966-110">Sensors that use optical scanning to read bar codes.</span></span><br/> |
| <span id="SENSOR_TYPE_RFID_SCANNER"></span><span id="sensor_type_rfid_scanner"></span><dl> <span data-ttu-id="54966-111"><dt>**Sensor \_ Geben Sie \_ RFID \_ Scanner**</dt> <dt>{44328ef5-02dd-4E8D-ad5d-9249832b2eca}</dt> ein.</span><span class="sxs-lookup"><span data-stu-id="54966-111"><dt>**SENSOR\_TYPE\_RFID\_SCANNER**</dt> <dt>{44328EF5-02DD-4E8D-AD5D-9249832B2ECA}</dt></span></span> </dl>          | <span data-ttu-id="54966-112">Sensoren für die Überprüfung der Funkfrequenz.</span><span class="sxs-lookup"><span data-stu-id="54966-112">Radio-frequency ID scanning sensors.</span></span><br/>                 |



<span data-ttu-id="54966-113">**Platt Form definierte Datenfelder**</span><span class="sxs-lookup"><span data-stu-id="54966-113">**Platform-Defined Data Fields**</span></span>

<span data-ttu-id="54966-114">Platt Form definierte Eigenschafts Schlüssel für diese Kategorie basieren auf dem Sensor- \_ \_ Datentyp \_ Scanner- \_ GUID:</span><span class="sxs-lookup"><span data-stu-id="54966-114">Platform-defined property keys for this category are based on SENSOR\_DATA\_TYPE\_SCANNER\_GUID:</span></span>

<span data-ttu-id="54966-115">{D7A59A3C-3421-44AB-8D3A-9DE8AB6C4CAE}</span><span class="sxs-lookup"><span data-stu-id="54966-115">{D7A59A3C-3421-44AB-8D3A-9DE8AB6C4CAE}</span></span>

<span data-ttu-id="54966-116">Diese Kategorie enthält die folgenden Platt Form definierten Datenfelder.</span><span class="sxs-lookup"><span data-stu-id="54966-116">This category includes the following platform-defined data fields.</span></span>



| <span data-ttu-id="54966-117">Name und PID des Daten Felds</span><span class="sxs-lookup"><span data-stu-id="54966-117">Data field name and PID</span></span>                                                                                                                                                                                                                                                                     | <span data-ttu-id="54966-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="54966-118">Description</span></span>                                                            |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_RFID_TAG_40_BIT"></span><span id="sensor_data_type_rfid_tag_40_bit"></span><dl> <span data-ttu-id="54966-119"><dt>**Sensor \_ \_Datentyp \_ RFID- \_ Tag \_ 40 \_ Bit**</dt> <dt>(PID = 2)</dt></span><span class="sxs-lookup"><span data-stu-id="54966-119"><dt>**SENSOR\_DATA\_TYPE\_RFID\_TAG\_40\_BIT**</dt> <dt>(PID = 2) </dt></span></span> </dl> | <span data-ttu-id="54966-120">**VT \_ UI8**</span><span class="sxs-lookup"><span data-stu-id="54966-120">**VT\_UI8**</span></span><br/> <span data-ttu-id="54966-121">40-Bit-Tagwert für Radio Frequency ID-Kennung.</span><span class="sxs-lookup"><span data-stu-id="54966-121">40-bit radio frequency ID tag value.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="54966-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="54966-122">Requirements</span></span>



| <span data-ttu-id="54966-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="54966-123">Requirement</span></span> | <span data-ttu-id="54966-124">Wert</span><span class="sxs-lookup"><span data-stu-id="54966-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="54966-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="54966-125">Minimum supported client</span></span><br/> | <span data-ttu-id="54966-126">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="54966-126">Windows 7 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="54966-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="54966-127">Minimum supported server</span></span><br/> | <span data-ttu-id="54966-128">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="54966-128">None supported</span></span><br/>                                                            |
| <span data-ttu-id="54966-129">Header</span><span class="sxs-lookup"><span data-stu-id="54966-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="54966-130"><dt>Sensoren. h</dt></span><span class="sxs-lookup"><span data-stu-id="54966-130"><dt>Sensors.h</dt></span></span> </dl> |



 

 




