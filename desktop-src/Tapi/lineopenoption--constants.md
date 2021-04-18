---
description: Die lineopenoption- \_ Konstanten listet die verfügbaren Optionen zum Öffnen einer Zeile auf.
ms.assetid: 361ae90c-a2cf-4107-a2da-80f561a82c56
title: LINEOPENOPTION_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dee9182ff7a28627eebd695ce5d9c0877460b15e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365726"
---
# <a name="lineopenoption_-constants"></a><span data-ttu-id="04050-103">Lineopenoption- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="04050-103">LINEOPENOPTION\_ Constants</span></span>

<span data-ttu-id="04050-104">Die **lineopenoption- \_ Konstanten** listet die verfügbaren Optionen zum Öffnen einer Zeile auf.</span><span class="sxs-lookup"><span data-stu-id="04050-104">The **LINEOPENOPTION\_ constants** list the available options for opening a line.</span></span>

<dl> <dt>

<span data-ttu-id="04050-105"><span id="LINEOPENOPTION_PROXY"></span><span id="lineopenoption_proxy"></span>**lineopenoption- \_ Proxy**</span><span class="sxs-lookup"><span data-stu-id="04050-105"><span id="LINEOPENOPTION_PROXY"></span><span id="lineopenoption_proxy"></span>**LINEOPENOPTION\_PROXY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="04050-106">Die Anwendung ist bereit, Anforderungen von anderen Anwendungen zu verarbeiten, für die die Zeile geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="04050-106">The application is willing to handle requests from other applications that have the line open.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="04050-107"><span id="LINEOPENOPTION_SINGLEADDRESS"></span><span id="lineopenoption_singleaddress"></span>**lineopenoption- \_ singleaddress**</span><span class="sxs-lookup"><span data-stu-id="04050-107"><span id="LINEOPENOPTION_SINGLEADDRESS"></span><span id="lineopenoption_singleaddress"></span>**LINEOPENOPTION\_SINGLEADDRESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="04050-108">Die Anwendung sollte nur über neue Aufrufe informiert werden, die auf dem Zeilen Gerät erstellt wurden, wenn diese Aufrufe für die Adresse angezeigt werden, die im Element " **dwadressssid** " in der [**linecallpara**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) -Struktur angegeben ist, auf die durch den *lpcallparameame-* Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="04050-108">The application should be informed of new calls created on the line device only if those calls appear on the address specified in the **dwAddressID** member in the [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) structure pointed to by the *lpCallParams* parameter.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="04050-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="04050-109">Remarks</span></span>

<span data-ttu-id="04050-110">Weitere Informationen zum Betrieb dieser Optionen finden Sie unter [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) .</span><span class="sxs-lookup"><span data-stu-id="04050-110">See [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) for further details on the operation of these options.</span></span>

## <a name="requirements"></a><span data-ttu-id="04050-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="04050-111">Requirements</span></span>



| <span data-ttu-id="04050-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="04050-112">Requirement</span></span> | <span data-ttu-id="04050-113">Wert</span><span class="sxs-lookup"><span data-stu-id="04050-113">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="04050-114">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="04050-114">TAPI version</span></span><br/> | <span data-ttu-id="04050-115">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="04050-115">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="04050-116">Header</span><span class="sxs-lookup"><span data-stu-id="04050-116">Header</span></span><br/>       | <dl> <span data-ttu-id="04050-117"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="04050-117"><dt>Tapi.h</dt></span></span> </dl> |



 

 




