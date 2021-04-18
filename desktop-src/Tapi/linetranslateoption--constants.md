---
description: Die \_ Bit-Flag-Konstante linetranslateoption beschreibt eine Option, die von der Adressübersetzung verwendet wird.
ms.assetid: 3f5e9952-945e-42b8-8536-b52a0c833282
title: LINETRANSLATEOPTION_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac1e103f2a93d30be5260b27c7bf5c0e97f3ce7a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372353"
---
# <a name="linetranslateoption_-constants"></a><span data-ttu-id="03821-103">Linetranslateoption- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="03821-103">LINETRANSLATEOPTION\_ Constants</span></span>

<span data-ttu-id="03821-104">Die Bit-Flag-Konstante **linetranslateoption \_** beschreibt eine Option, die von der Adressübersetzung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="03821-104">The **LINETRANSLATEOPTION\_** bit-flag constant describes an option used by address translation.</span></span>

<dl> <dt>

<span data-ttu-id="03821-105"><span id="LINETRANSLATEOPTION_CANCELCALLWAITING"></span><span id="linetranslateoption_cancelcallwaiting"></span>**linetranslateoption \_ cancelcallwaiting**</span><span class="sxs-lookup"><span data-stu-id="03821-105"><span id="LINETRANSLATEOPTION_CANCELCALLWAITING"></span><span id="linetranslateoption_cancelcallwaiting"></span>**LINETRANSLATEOPTION\_CANCELCALLWAITING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="03821-106">Wenn eine aufrufende Zeichenfolge für den Abbruch Aufruf für den Speicherort definiert ist, bewirkt das Festlegen dieses Bits, dass diese Zeichenfolge am Anfang der ausführbaren Zeichenfolge eingefügt wird.</span><span class="sxs-lookup"><span data-stu-id="03821-106">If a Cancel Call Waiting string is defined for the location, setting this bit will cause that string to be inserted at the beginning of the dialable string.</span></span> <span data-ttu-id="03821-107">Dies wird häufig von Datenmodem-und Faxanwendungen verwendet, um die Unterbrechung von Aufrufen durch Aufrufe, die darauf warten, zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="03821-107">This is commonly used by data modem and fax applications to prevent interruption of calls by call waiting beeps.</span></span> <span data-ttu-id="03821-108">Wenn keine aufrufende Zeichenfolge für den Abbruch Vorgang für den Speicherort definiert ist, hat dieses Bit keine Auswirkung.</span><span class="sxs-lookup"><span data-stu-id="03821-108">If no Cancel Call Waiting string is defined for the location, this bit has no affect.</span></span> <span data-ttu-id="03821-109">Beachten Sie, dass für Anwendungen, die dieses Bit verwenden, empfohlen wird, auch das Secure-Bit linecallparamflags \_ im **dwcallparamflags** -Member der [**linecallpara**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) -Struktur festzulegen, die über den *lpcallparser* -Parameter an [**linemakecall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) übergeben wird, sodass der Mechanismus aufgerufen wird, wenn das liniengerät einen anderen Mechanismus als dable-Ziffern verwendet.</span><span class="sxs-lookup"><span data-stu-id="03821-109">Note that applications using this bit are advised to also set the LINECALLPARAMFLAGS\_SECURE bit in the **dwCallParamFlags** member of the [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) structure passed in to [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) through the *lpCallParams* parameter, so that if the line device uses a mechanism other than dialable digits to suppress call interrupts then that mechanism will be invoked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="03821-110"><span id="LINETRANSLATEOPTION_CARDOVERRIDE"></span><span id="linetranslateoption_cardoverride"></span>**linetranslateoption \_ cardoverride**</span><span class="sxs-lookup"><span data-stu-id="03821-110"><span id="LINETRANSLATEOPTION_CARDOVERRIDE"></span><span id="linetranslateoption_cardoverride"></span>**LINETRANSLATEOPTION\_CARDOVERRIDE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="03821-111">Die Standard Aufruf Karte muss mit einem angegebenen überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="03821-111">The default calling card is to be overridden with a specified one.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="03821-112"><span id="LINETRANSLATEOPTION_FORCELD"></span><span id="linetranslateoption_forceld"></span>**linetranslateoption ( \_ forceld)**</span><span class="sxs-lookup"><span data-stu-id="03821-112"><span id="LINETRANSLATEOPTION_FORCELD"></span><span id="linetranslateoption_forceld"></span>**LINETRANSLATEOPTION\_FORCELD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="03821-113">Diese Option erzwingt, dass die Adresse (Zahl) als lange Distanz übersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="03821-113">This option forces the address (number) to be translated as long distance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="03821-114"><span id="LINETRANSLATEOPTION_FORCELOCAL"></span><span id="linetranslateoption_forcelocal"></span>**linetranslateoption ( \_ forcelocal)**</span><span class="sxs-lookup"><span data-stu-id="03821-114"><span id="LINETRANSLATEOPTION_FORCELOCAL"></span><span id="linetranslateoption_forcelocal"></span>**LINETRANSLATEOPTION\_FORCELOCAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="03821-115">Diese Option erzwingt, dass die Zahl (Address) als Local übersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="03821-115">This option forces the number (address) to be translated as local.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="03821-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="03821-116">Remarks</span></span>

<span data-ttu-id="03821-117">Keine Erweiterbarkeit.</span><span class="sxs-lookup"><span data-stu-id="03821-117">No extensibility.</span></span> <span data-ttu-id="03821-118">Alle 32 Bits sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="03821-118">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="03821-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="03821-119">Requirements</span></span>



| <span data-ttu-id="03821-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="03821-120">Requirement</span></span> | <span data-ttu-id="03821-121">Wert</span><span class="sxs-lookup"><span data-stu-id="03821-121">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="03821-122">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="03821-122">TAPI version</span></span><br/> | <span data-ttu-id="03821-123">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="03821-123">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="03821-124">Header</span><span class="sxs-lookup"><span data-stu-id="03821-124">Header</span></span><br/>       | <dl> <span data-ttu-id="03821-125"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="03821-125"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03821-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="03821-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03821-127">**Linecallparametriams**</span><span class="sxs-lookup"><span data-stu-id="03821-127">**LINECALLPARAMS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallparams)
</dt> <dt>

[<span data-ttu-id="03821-128">**linemakecall**</span><span class="sxs-lookup"><span data-stu-id="03821-128">**lineMakeCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[<span data-ttu-id="03821-129">**Linetranslateoutput**</span><span class="sxs-lookup"><span data-stu-id="03821-129">**LINETRANSLATEOUTPUT**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linetranslateoutput)
</dt> </dl>

 

 




