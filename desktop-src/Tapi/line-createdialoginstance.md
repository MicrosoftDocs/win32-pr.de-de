---
description: Die TSPI-Zeile " \_ foratedialoginstance" bewirkt, dass TAPI eine Zuordnung zwischen dem Dienstanbieter und einer Instanz der "tuispi \_ providergenericdialog"-Funktion erstellt, die im Kontext der Anwendung ausgeführt wird.
ms.assetid: 5a7e34bc-1dc3-40c4-b07e-de5b88cbcd75
title: LINE_CREATEDIALOGINSTANCE Meldung (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c92088b79bdd085874d14817e6e9652f03c6c00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351319"
---
# <a name="line_createdialoginstance-message"></a><span data-ttu-id="12d09-103">Zeile "" mit der Meldung "". \_</span><span class="sxs-lookup"><span data-stu-id="12d09-103">LINE\_CREATEDIALOGINSTANCE message</span></span>

<span data-ttu-id="12d09-104">Die TSPI- **Zeile " \_ foratedialoginstance** " bewirkt, dass TAPI eine Zuordnung zwischen dem Dienstanbieter und einer Instanz der " [**tuispi \_ providergenericdialog**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog) "-Funktion erstellt, die im Kontext der Anwendung ausgeführt wird, die die asyndie Chrone TSPI-Funktion, die durch den *dwrequestid-* Parameter der [**tuispikreatedialoginstanceparameginstancepara**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams) -Struktur identifiziert wird, auf die von *lptuispikreatedialoginstanceparameams* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="12d09-104">The TSPI **LINE\_CREATEDIALOGINSTANCE** message causes TAPI to create an association between the service provider and an instance of the [**TUISPI\_providerGenericDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog) function executing in the context of the application that invoked the asynchronous TSPI function identified by the *dwRequestID* parameter of the [**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams) structure pointed to by *lpTUISPICreateDialogInstanceParams*.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="12d09-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="12d09-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12d09-106">*hprovider*</span><span class="sxs-lookup"><span data-stu-id="12d09-106">*hProvider*</span></span> 
</dt> <dd>

<span data-ttu-id="12d09-107">Das ProviderHandle, das für den Dienstanbieter als Parameter für [**TSPI \_ providerenumdevices**](/windows/win32/api/tspi/nf-tspi-tspi_providerenumdevices)bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="12d09-107">The ProviderHandle supplied to the service provider as a parameter to [**TSPI\_providerEnumDevices**](/windows/win32/api/tspi/nf-tspi-tspi_providerenumdevices).</span></span>

</dd> <dt>

<span data-ttu-id="12d09-108">*lptuispikreatedialoginstanceparameams*</span><span class="sxs-lookup"><span data-stu-id="12d09-108">*lpTUISPICreateDialogInstanceParams*</span></span> 
</dt> <dd>

<span data-ttu-id="12d09-109">Zeiger auf die Struktur " [**tuispikreatedialoginstanceparameginstanceparameginstancepara**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams)</span><span class="sxs-lookup"><span data-stu-id="12d09-109">Pointer to a [**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams) structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="12d09-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="12d09-110">Requirements</span></span>



| <span data-ttu-id="12d09-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="12d09-111">Requirement</span></span> | <span data-ttu-id="12d09-112">Wert</span><span class="sxs-lookup"><span data-stu-id="12d09-112">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="12d09-113">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="12d09-113">TAPI version</span></span><br/> | <span data-ttu-id="12d09-114">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="12d09-114">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="12d09-115">Header</span><span class="sxs-lookup"><span data-stu-id="12d09-115">Header</span></span><br/>       | <dl> <span data-ttu-id="12d09-116"><dt>TSPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="12d09-116"><dt>Tspi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12d09-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="12d09-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12d09-118">**TSPI \_ providerenumdevices**</span><span class="sxs-lookup"><span data-stu-id="12d09-118">**TSPI\_providerEnumDevices**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerenumdevices)
</dt> <dt>

[<span data-ttu-id="12d09-119">**"Tuispikreatedialoginstanceparameginstancepara"**</span><span class="sxs-lookup"><span data-stu-id="12d09-119">**TUISPICREATEDIALOGINSTANCEPARAMS**</span></span>](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams)
</dt> </dl>

 

