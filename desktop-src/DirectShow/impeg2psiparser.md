---
description: Die Implementierung dieser Schnittstelle wird als Beispielcode mit dem DirectShow SDK bereitgestellt.
ms.assetid: a18fc6b6-f37e-4c87-9150-0504333d33c2
title: IMpeg2PsiParser-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser
api_type:
- COM
api_location: ''
ms.openlocfilehash: 51f0f3373c67da75c50ecc2f6bc234e0351f5dc3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106342720"
---
# <a name="impeg2psiparser-interface"></a><span data-ttu-id="f04b0-103">IMpeg2PsiParser-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f04b0-103">IMpeg2PsiParser interface</span></span>

<span data-ttu-id="f04b0-104">Die Implementierung dieser Schnittstelle wird als Beispielcode mit dem DirectShow SDK bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="f04b0-104">The implementation of this interface is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="f04b0-105">Es handelt sich nicht um eine unterstützte DirectShow-API.</span><span class="sxs-lookup"><span data-stu-id="f04b0-105">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="f04b0-106">Die- `IMpeg2PsiParser` Schnittstelle ruft Programm spezifische Informationen (PSI) aus dem PSI-Parser-Filter ab, der im DirectShow SDK als Beispiel Filter bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="f04b0-106">The `IMpeg2PsiParser` interface retrieves Program Specific Information (PSI) from the PSI Parser filter, which is provided in the DirectShow SDK as a sample filter.</span></span> <span data-ttu-id="f04b0-107">Eine Anwendung kann diesen Filter verwenden, um Programm-IDs (PIDs) dem MPEG-2-Demultiplexer-Filter zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="f04b0-107">An application can use this filter to map program IDs (PIDs) on the MPEG-2 Demultiplexer filter.</span></span>

## <a name="members"></a><span data-ttu-id="f04b0-108">Member</span><span class="sxs-lookup"><span data-stu-id="f04b0-108">Members</span></span>

<span data-ttu-id="f04b0-109">Die **IMpeg2PsiParser** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f04b0-109">The **IMpeg2PsiParser** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f04b0-110">**IMpeg2PsiParser** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f04b0-110">**IMpeg2PsiParser** also has these types of members:</span></span>

-   [<span data-ttu-id="f04b0-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="f04b0-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f04b0-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="f04b0-112">Methods</span></span>

<span data-ttu-id="f04b0-113">Die **IMpeg2PsiParser** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="f04b0-113">The **IMpeg2PsiParser** interface has these methods.</span></span>



| <span data-ttu-id="f04b0-114">Methode</span><span class="sxs-lookup"><span data-stu-id="f04b0-114">Method</span></span>                                                                             | <span data-ttu-id="f04b0-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f04b0-115">Description</span></span>                                                                               |
|:-----------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| <span data-ttu-id="f04b0-116">[**Findrecordprogrammappid**](/previous-versions/windows/desktop/legacy/dd407137(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f04b0-116">[**FindRecordProgramMapPid**](/previous-versions/windows/desktop/legacy/dd407137(v=vs.85))</span></span>         | <span data-ttu-id="f04b0-117">Sucht die PMT-PID (Program Map Table) für ein Programm, sofern die Programmnummer angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="f04b0-117">Finds the Program Map Table (PMT) PID for a program, given the program number.</span></span><br/> |
| [<span data-ttu-id="f04b0-118">**Getzähltofelementarystreams**</span><span class="sxs-lookup"><span data-stu-id="f04b0-118">**GetCountOfElementaryStreams**</span></span>](impeg2psiparser-getcountofelementarystreams.md) | <span data-ttu-id="f04b0-119">Ruft die Anzahl der elementaren Datenströme in einem angegebenen Programm ab.</span><span class="sxs-lookup"><span data-stu-id="f04b0-119">Retrieves the number of elementary streams in a specified program.</span></span><br/>             |
| [<span data-ttu-id="f04b0-120">**Getgräfin-Druck Programme**</span><span class="sxs-lookup"><span data-stu-id="f04b0-120">**GetCountOfPrograms**</span></span>](impeg2psiparser-getcountofprograms.md)                   | <span data-ttu-id="f04b0-121">Ruft die Anzahl der Programme im Transportstream ab.</span><span class="sxs-lookup"><span data-stu-id="f04b0-121">Retrieves the number of programs in the transport stream.</span></span><br/>                      |
| [<span data-ttu-id="f04b0-122">**Getpatversionnumber**</span><span class="sxs-lookup"><span data-stu-id="f04b0-122">**GetPatVersionNumber**</span></span>](impeg2psiparser-getpatversionnumber.md)                 | <span data-ttu-id="f04b0-123">Ruft das Feld mit der Versions \_ Nummer aus der Programm Zuordnungs Tabelle (Pat) ab.</span><span class="sxs-lookup"><span data-stu-id="f04b0-123">Retrieves the version\_number field from the Program Association Table (PAT).</span></span><br/>  |
| [<span data-ttu-id="f04b0-124">**Getpmtversionnumber**</span><span class="sxs-lookup"><span data-stu-id="f04b0-124">**GetPmtVersionNumber**</span></span>](impeg2psiparser-getpmtversionnumber.md)                 | <span data-ttu-id="f04b0-125">Ruft das Feld der Versions \_ Nummer von einem angegebenen PMT ab.</span><span class="sxs-lookup"><span data-stu-id="f04b0-125">Retrieves the version\_number field from a specified PMT.</span></span><br/>                      |
| <span data-ttu-id="f04b0-126">[**Getrecorschementarypid**](/previous-versions/windows/desktop/legacy/dd376623(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f04b0-126">[**GetRecordElementaryPid**](/previous-versions/windows/desktop/legacy/dd376623(v=vs.85))</span></span>           | <span data-ttu-id="f04b0-127">Ruft die PID-Zuweisung für einen angegebenen elementaren Stream in einem Programm ab.</span><span class="sxs-lookup"><span data-stu-id="f04b0-127">Retrieves the PID assignment for a specified elementary stream in a program.</span></span><br/>   |
| <span data-ttu-id="f04b0-128">[**Getrecordprogrammappid**](/previous-versions/windows/desktop/legacy/dd376624(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f04b0-128">[**GetRecordProgramMapPid**](/previous-versions/windows/desktop/legacy/dd376624(v=vs.85))</span></span>           | <span data-ttu-id="f04b0-129">Ruft die PID-Zuweisung für ein angegebenes PMT ab.</span><span class="sxs-lookup"><span data-stu-id="f04b0-129">Retrieves the PID assignment for a specified PMT.</span></span><br/>                              |
| [<span data-ttu-id="f04b0-130">**Getrecordprogramnumber**</span><span class="sxs-lookup"><span data-stu-id="f04b0-130">**GetRecordProgramNumber**</span></span>](impeg2psiparser-getrecordprogramnumber.md)           | <span data-ttu-id="f04b0-131">Ruft die Programmnummer für ein angegebenes Programm ab.</span><span class="sxs-lookup"><span data-stu-id="f04b0-131">Retrieves the program number for a specified program.</span></span><br/>                          |
| <span data-ttu-id="f04b0-132">[**Getrecordstreamtype**](/previous-versions/windows/desktop/legacy/dd376626(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f04b0-132">[**GetRecordStreamType**](/previous-versions/windows/desktop/legacy/dd376626(v=vs.85))</span></span>                 | <span data-ttu-id="f04b0-133">Ruft den Streamtyp für einen angegebenen elementaren Stream in einem Programm ab.</span><span class="sxs-lookup"><span data-stu-id="f04b0-133">Retrieves the stream type for a specified elementary stream in a program.</span></span><br/>      |
| [<span data-ttu-id="f04b0-134">**Gettransportstreamid**</span><span class="sxs-lookup"><span data-stu-id="f04b0-134">**GetTransportStreamId**</span></span>](impeg2psiparser-gettransportstreamid.md)               | <span data-ttu-id="f04b0-135">Ruft das Transportdaten \_ Strom- \_ ID-Feld aus der PAT-Datei ab.</span><span class="sxs-lookup"><span data-stu-id="f04b0-135">Retrieves the transport\_stream\_id field from the PAT.</span></span><br/>                        |



 

## <a name="see-also"></a><span data-ttu-id="f04b0-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f04b0-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f04b0-137">Beispiel für PSI-Parser-Filter</span><span class="sxs-lookup"><span data-stu-id="f04b0-137">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 
