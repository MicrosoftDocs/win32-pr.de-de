---
description: Die TSPI-Zeile \_ senddialoginstancedata bewirkt, dass TAPI die Funktion "tuispi \_ providergenericdialogdata" in der Benutzeroberflächen-DLL aufruft, die mit "htdlginst" verknüpft ist, und übergibt dabei den Parameter Block, auf den lpparser zeigt, mit der Länge "dwSize".
ms.assetid: d3c176ba-8b4b-4b7c-a603-130dfa761898
title: LINE_SENDDIALOGINSTANCEDATA Meldung (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0af7ae5bfc942d4408ac5ce2438cd9a88c1f1f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371327"
---
# <a name="line_senddialoginstancedata-message"></a><span data-ttu-id="aa1fa-103">Zeile \_ senddialoginstancedata</span><span class="sxs-lookup"><span data-stu-id="aa1fa-103">LINE\_SENDDIALOGINSTANCEDATA message</span></span>

<span data-ttu-id="aa1fa-104">Die TSPI **-Zeile \_ senddialoginstancedata** bewirkt, dass TAPI die Funktion " [**tuispi \_ providergenericdialogdata**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata) " in der Benutzeroberflächen-DLL aufruft, die mit " *htdlginst*" verknüpft ist, und übergibt dabei den Parameter Block, auf den *lpparser* zeigt, mit der Länge " *dwSize*".</span><span class="sxs-lookup"><span data-stu-id="aa1fa-104">The TSPI **LINE\_SENDDIALOGINSTANCEDATA** message causes TAPI to call the [**TUISPI\_providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata) function in the UI DLL associated with *htDlgInst*, passing it the parameter block pointed to by *lpParams*, of length *dwSize*.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="aa1fa-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa1fa-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa1fa-106">*"htdlginst"*</span><span class="sxs-lookup"><span data-stu-id="aa1fa-106">*htDlgInst*</span></span> 
</dt> <dd>

<span data-ttu-id="aa1fa-107">Die htapidialoginstance, die an den Dienstanbieter zurückgegeben wurde, als die Dialogfeld Instanz mithilfe der Zeile ' ' erstellt wurde. [**\_**](line-createdialoginstance.md)</span><span class="sxs-lookup"><span data-stu-id="aa1fa-107">The HTAPIDIALOGINSTANCE that was returned to the service provider when the dialog box instance was created using [**LINE\_CREATEDIALOGINSTANCE**](line-createdialoginstance.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa1fa-108">*lpparser*</span><span class="sxs-lookup"><span data-stu-id="aa1fa-108">*lpParams*</span></span> 
</dt> <dd>

<span data-ttu-id="aa1fa-109">Ein Zeiger auf einen anbieterspezifischen Parameter Block, der der Benutzeroberflächen-DLL-Funktion " [**tuispi \_ providergenericdialogdata**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata) " übermittelt wird, deren Größe von *dwSize* angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="aa1fa-109">Pointer to a provider-specific parameter block that is conveyed to the UI DLL [**TUISPI\_providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata) function, the size of which is specified by *dwSize*.</span></span> <span data-ttu-id="aa1fa-110">Wenn dieser Parameter auf **null** festgelegt ist, ist dies eine Anforderung zum sofortigen Schließen des Dialog Felds und zum Bereinigen (die Benutzeroberflächen-DLL sollte während dieser Bereinigung nicht " [**tuispidllcallback**](/windows/win32/api/tspi/nc-tspi-tuispidllcallback) " aufrufen).</span><span class="sxs-lookup"><span data-stu-id="aa1fa-110">If this parameter is set to **NULL**, this is a request to close the dialog box immediately and clean up (the UI DLL should not invoke [**TUISPIDLLCALLBACK**](/windows/win32/api/tspi/nc-tspi-tuispidllcallback) during this cleanup).</span></span>

</dd> <dt>

<span data-ttu-id="aa1fa-111">*dwSize*</span><span class="sxs-lookup"><span data-stu-id="aa1fa-111">*dwSize*</span></span> 
</dt> <dd>

<span data-ttu-id="aa1fa-112">Die Größe des Parameter Blocks in Bytes, der an die Benutzeroberflächen-DLL übermittelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="aa1fa-112">The size in bytes of the parameter block to be conveyed to the UI DLL.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="aa1fa-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aa1fa-113">Requirements</span></span>



| <span data-ttu-id="aa1fa-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aa1fa-114">Requirement</span></span> | <span data-ttu-id="aa1fa-115">Wert</span><span class="sxs-lookup"><span data-stu-id="aa1fa-115">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="aa1fa-116">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="aa1fa-116">TAPI version</span></span><br/> | <span data-ttu-id="aa1fa-117">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="aa1fa-117">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="aa1fa-118">Header</span><span class="sxs-lookup"><span data-stu-id="aa1fa-118">Header</span></span><br/>       | <dl> <span data-ttu-id="aa1fa-119"><dt>TSPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa1fa-119"><dt>Tspi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa1fa-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aa1fa-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa1fa-121">**Tuispidllcallback**</span><span class="sxs-lookup"><span data-stu-id="aa1fa-121">**TUISPIDLLCALLBACK**</span></span>](/windows/win32/api/tspi/nc-tspi-tuispidllcallback)
</dt> <dt>

[<span data-ttu-id="aa1fa-122">**Tuispi \_ providergenericdialogdata**</span><span class="sxs-lookup"><span data-stu-id="aa1fa-122">**TUISPI\_providerGenericDialogData**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata)
</dt> <dt>

[<span data-ttu-id="aa1fa-123">**Zeile " \_ kreatedialoginstance"**</span><span class="sxs-lookup"><span data-stu-id="aa1fa-123">**LINE\_CREATEDIALOGINSTANCE**</span></span>](line-createdialoginstance.md)
</dt> </dl>

 

