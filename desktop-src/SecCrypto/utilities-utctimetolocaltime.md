---
description: Konvertiert die koordinierte Weltzeit (Greenwich Mean Time) in die Ortszeit des Computers.
ms.assetid: 4085d7cb-d346-477d-a043-e96fb951c35a
title: Utilities. utctimetolocaltime-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.UTCTimeToLocalTime
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: fe41cf8d9ec92c0c71be5130aded0b7db539b9b1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361265"
---
# <a name="utilitiesutctimetolocaltime-method"></a><span data-ttu-id="a6f5f-103">Utilities. utctimetolocaltime-Methode</span><span class="sxs-lookup"><span data-stu-id="a6f5f-103">Utilities.UTCTimeToLocalTime method</span></span>

<span data-ttu-id="a6f5f-104">\[Die **utctimetolocaltime** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.\]</span><span class="sxs-lookup"><span data-stu-id="a6f5f-104">\[The **UTCTimeToLocalTime** method is available for use in the operating systems specified in the Requirements section.\]</span></span>

<span data-ttu-id="a6f5f-105">Die **utctimetolocaltime** -Methode konvertiert die koordinierte Weltzeit (Greenwich Mean Time) in die Ortszeit des Computers.</span><span class="sxs-lookup"><span data-stu-id="a6f5f-105">The **UTCTimeToLocalTime** method converts Coordinated Universal Time (Greenwich Mean Time) to the computer's local time.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6f5f-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a6f5f-106">Syntax</span></span>


```VB
Utilities.UTCTimeToLocalTime( _
  ByVal UTCTime _
)
```



## <a name="parameters"></a><span data-ttu-id="a6f5f-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="a6f5f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6f5f-108">*UtcTime* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a6f5f-108">*UTCTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6f5f-109">Die koordinierte Weltzeit, die in die lokale Zeit des Computers konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a6f5f-109">The Coordinated Universal Time to be converted to the computer's local time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6f5f-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a6f5f-110">Return value</span></span>

<span data-ttu-id="a6f5f-111">Die Ortszeit, die der angegebenen koordinierten Weltzeit entspricht.</span><span class="sxs-lookup"><span data-stu-id="a6f5f-111">The local time that corresponds to the specified Coordinated Universal Time.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6f5f-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a6f5f-112">Remarks</span></span>

<span data-ttu-id="a6f5f-113">Während das System eine koordinierte Weltzeit intern verwendet, zeigen Anwendungen in der Regel die Ortszeit an, die das Datum und die Uhrzeit für die lokale Zeitzone des Computers ist.</span><span class="sxs-lookup"><span data-stu-id="a6f5f-113">While the system uses Coordinated Universal Time internally, applications generally display the local time, which is the date and time of day for the computer's local time zone.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6f5f-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a6f5f-114">Requirements</span></span>



| <span data-ttu-id="a6f5f-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a6f5f-115">Requirement</span></span> | <span data-ttu-id="a6f5f-116">Wert</span><span class="sxs-lookup"><span data-stu-id="a6f5f-116">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a6f5f-117">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="a6f5f-117">Redistributable</span></span><br/> | <span data-ttu-id="a6f5f-118">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="a6f5f-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a6f5f-119">DLL</span><span class="sxs-lookup"><span data-stu-id="a6f5f-119">DLL</span></span><br/>             | <dl> <span data-ttu-id="a6f5f-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6f5f-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6f5f-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a6f5f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6f5f-122">**Versorgungsunternehmen**</span><span class="sxs-lookup"><span data-stu-id="a6f5f-122">**Utilities**</span></span>](utilities.md)
</dt> </dl>

 

 




