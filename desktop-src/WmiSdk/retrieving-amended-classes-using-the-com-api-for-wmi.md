---
description: 'Wenn Sie die com-API für WMI verwenden, um lokalisierte Klassen Informationen abzurufen oder zu speichern, geben Sie das Gebiets Schema im Parameter "strinlocale" an die IWbemLocator:: ConnectServer-Schnittstelle an.'
ms.assetid: 940a7bd9-c2ea-4deb-b5d8-207a0ce7a616
ms.tgt_platform: multiple
title: Abrufen von geänderten Klassen mithilfe der com-API für WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0178b0b99de2b666e2f497074a02b02c49ba400
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759762"
---
# <a name="retrieving-amended-classes-using-the-com-api-for-wmi"></a><span data-ttu-id="04e41-103">Abrufen von geänderten Klassen mithilfe der com-API für WMI</span><span class="sxs-lookup"><span data-stu-id="04e41-103">Retrieving Amended Classes Using the COM API for WMI</span></span>

<span data-ttu-id="04e41-104">Wenn Sie die com-API für WMI verwenden, um lokalisierte Klassen Informationen abzurufen oder zu speichern, geben Sie das Gebiets Schema im Parameter " *strinlocale* " an die [**IWBEMLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) -Schnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="04e41-104">If you are using the COM API for WMI to retrieve or store localized class information, specify the locale in the *strLocale* parameter to the [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) interface.</span></span> <span data-ttu-id="04e41-105">Beim Lesen oder Schreiben von geänderten Klassen geben Sie an, dass Sie lokalisierte Klassendefinitionen verwenden möchten, indem Sie das WBEM- \_ Flag \_ zum Verwenden von \_ geänderten \_ *Qualifizierern* als Flag für den IFlags-Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="04e41-105">When reading or writing amended classes, indicate that you want to use localized class definitions by specifying WBEM\_FLAG\_USE\_AMENDED\_QUALIFIERS as a flag for the *iFlags* parameter.</span></span>

<span data-ttu-id="04e41-106">In der folgenden Tabelle werden die synchronen und asynchronen Versionen der Methoden aufgelistet, die mit dem WBEM-Flag das Flag für \_ \_ \_ geänderte \_ Qualifizierer verwenden.</span><span class="sxs-lookup"><span data-stu-id="04e41-106">The following table lists the synchronous and asynchronous versions of the methods that use the WBEM\_FLAG\_USE\_AMENDED\_QUALIFIERS flag.</span></span>



| <span data-ttu-id="04e41-107">Synchrone Methode</span><span class="sxs-lookup"><span data-stu-id="04e41-107">Synchronous Method</span></span>                                                            | <span data-ttu-id="04e41-108">Asynchrone Methode</span><span class="sxs-lookup"><span data-stu-id="04e41-108">Asynchronous Method</span></span>                                                                     |
|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="04e41-109">**IWbemServices:: kreateclassenum**</span><span class="sxs-lookup"><span data-stu-id="04e41-109">**IWbemServices::CreateClassEnum**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum)       | [<span data-ttu-id="04e41-110">**IWbemServices:: "kreateclassenumschlag"**</span><span class="sxs-lookup"><span data-stu-id="04e41-110">**IWbemServices::CreateClassEnumAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync)       |
| [<span data-ttu-id="04e41-111">**IWbemServices:: kreateinstanceaufumum**</span><span class="sxs-lookup"><span data-stu-id="04e41-111">**IWbemServices::CreateInstanceEnum**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum) | [<span data-ttu-id="04e41-112">**IWbemServices:: kreateingestanceenumasync**</span><span class="sxs-lookup"><span data-stu-id="04e41-112">**IWbemServices::CreateInstanceEnumAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) |
| [<span data-ttu-id="04e41-113">**IWbemServices:: ExecQuery**</span><span class="sxs-lookup"><span data-stu-id="04e41-113">**IWbemServices::ExecQuery**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery)                   | [<span data-ttu-id="04e41-114">**IWbemServices:: ExecQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="04e41-114">**IWbemServices::ExecQueryAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)                   |
| [<span data-ttu-id="04e41-115">**IWbemServices:: GetObject**</span><span class="sxs-lookup"><span data-stu-id="04e41-115">**IWbemServices::GetObject**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)                   | [<span data-ttu-id="04e41-116">**IWbemServices:: GetObjectAsync**</span><span class="sxs-lookup"><span data-stu-id="04e41-116">**IWbemServices::GetObjectAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)                   |
| [<span data-ttu-id="04e41-117">**IWbemServices::P utclass**</span><span class="sxs-lookup"><span data-stu-id="04e41-117">**IWbemServices::PutClass**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass)                     | [<span data-ttu-id="04e41-118">**IWbemServices::P utclassasync**</span><span class="sxs-lookup"><span data-stu-id="04e41-118">**IWbemServices::PutClassAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync)                     |
| [<span data-ttu-id="04e41-119">**IWbemServices::P utinstance**</span><span class="sxs-lookup"><span data-stu-id="04e41-119">**IWbemServices::PutInstance**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance)               | [<span data-ttu-id="04e41-120">**IWbemServices::P utinstanceasync**</span><span class="sxs-lookup"><span data-stu-id="04e41-120">**IWbemServices::PutInstanceAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)               |



 

 

 



