---
description: Konvertiert die lokale Zeit des Computers in eine koordinierte Weltzeit (Greenwich Mean Time).
ms.assetid: ff5d40ba-7d94-4f11-9c18-e41752d1d7b9
title: Utilities. localtimetoutctime-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.LocalTimeToUTCTime
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2691e3306a84ce4eff3d73df4b070ba4b65671f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355857"
---
# <a name="utilitieslocaltimetoutctime-method"></a><span data-ttu-id="8d44c-103">Utilities. localtimetoutctime-Methode</span><span class="sxs-lookup"><span data-stu-id="8d44c-103">Utilities.LocalTimeToUTCTime method</span></span>

<span data-ttu-id="8d44c-104">\[Die **localtimetoutctime** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.\]</span><span class="sxs-lookup"><span data-stu-id="8d44c-104">\[The **LocalTimeToUTCTime** method is available for use in the operating systems specified in the Requirements section.\]</span></span>

<span data-ttu-id="8d44c-105">Die **localtimetoutctime** -Methode konvertiert die lokale Zeit des Computers in eine koordinierte Weltzeit (Greenwich Mean Time).</span><span class="sxs-lookup"><span data-stu-id="8d44c-105">The **LocalTimeToUTCTime** method converts the computer's local time to Coordinated Universal Time (Greenwich Mean Time).</span></span>

## <a name="syntax"></a><span data-ttu-id="8d44c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="8d44c-106">Syntax</span></span>


```VB
Utilities.LocalTimeToUTCTime( _
  ByVal LocalTime _
)
```



## <a name="parameters"></a><span data-ttu-id="8d44c-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d44c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d44c-108">*Localtime* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8d44c-108">*LocalTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d44c-109">Die Ortszeit, die in die koordinierte Weltzeit konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="8d44c-109">The local time to be converted to Coordinated Universal Time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d44c-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8d44c-110">Return value</span></span>

<span data-ttu-id="8d44c-111">Die koordinierte Weltzeit, die der angegebenen Ortszeit entspricht.</span><span class="sxs-lookup"><span data-stu-id="8d44c-111">The Coordinated Universal Time that corresponds to the specified local time.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d44c-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8d44c-112">Remarks</span></span>

<span data-ttu-id="8d44c-113">Während das System eine koordinierte Weltzeit intern verwendet, zeigen Anwendungen in der Regel die Ortszeit an, die das Datum und die Uhrzeit für die lokale Zeitzone des Computers ist.</span><span class="sxs-lookup"><span data-stu-id="8d44c-113">While the system uses Coordinated Universal Time internally, applications generally display the local time, which is the date and time of day for the computer's local time zone.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d44c-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8d44c-114">Requirements</span></span>



| <span data-ttu-id="8d44c-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8d44c-115">Requirement</span></span> | <span data-ttu-id="8d44c-116">Wert</span><span class="sxs-lookup"><span data-stu-id="8d44c-116">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d44c-117">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="8d44c-117">Redistributable</span></span><br/> | <span data-ttu-id="8d44c-118">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="8d44c-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="8d44c-119">DLL</span><span class="sxs-lookup"><span data-stu-id="8d44c-119">DLL</span></span><br/>             | <dl> <span data-ttu-id="8d44c-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d44c-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d44c-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8d44c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d44c-122">**Versorgungsunternehmen**</span><span class="sxs-lookup"><span data-stu-id="8d44c-122">**Utilities**</span></span>](utilities.md)
</dt> </dl>

 

 




