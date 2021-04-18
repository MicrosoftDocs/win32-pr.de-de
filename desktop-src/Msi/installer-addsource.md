---
description: Die addsource-Methode des Installer-Objekts fügt der Liste der gültigen Netzwerk Quellen in der SourceList eine Quelle hinzu.
ms.assetid: e24c8484-fe84-4f97-9c06-c063bb7c6810
title: Installer. addsource-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.AddSource
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3067ae287311c6ed26b509545523db75a3fed4cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372391"
---
# <a name="installeraddsource-method"></a><span data-ttu-id="4955f-103">Installer. addsource-Methode</span><span class="sxs-lookup"><span data-stu-id="4955f-103">Installer.AddSource method</span></span>

<span data-ttu-id="4955f-104">Die **addsource** -Methode des [**Installer**](installer-object.md) -Objekts fügt der Liste der gültigen Netzwerk Quellen in der SourceList eine Quelle hinzu.</span><span class="sxs-lookup"><span data-stu-id="4955f-104">The **AddSource** method of the [**Installer**](installer-object.md) object adds a source to the list of valid network sources in the sourcelist.</span></span>

## <a name="syntax"></a><span data-ttu-id="4955f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4955f-105">Syntax</span></span>


```JScript
Installer.AddSource(
  Product,
  User,
  Source
)
```



## <a name="parameters"></a><span data-ttu-id="4955f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4955f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4955f-107">*Produkt*</span><span class="sxs-lookup"><span data-stu-id="4955f-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="4955f-108">Gibt den Produktcode an.</span><span class="sxs-lookup"><span data-stu-id="4955f-108">Specifies the product code.</span></span>

</dd> <dt>

<span data-ttu-id="4955f-109">*Benutzer*</span><span class="sxs-lookup"><span data-stu-id="4955f-109">*User*</span></span> 
</dt> <dd>

<span data-ttu-id="4955f-110">Benutzername für die Installation pro Benutzer NULL oder eine leere Zeichenfolge für die Installation pro Computer.</span><span class="sxs-lookup"><span data-stu-id="4955f-110">User name for per-user installation; null or empty string for per-machine installation.</span></span>

</dd> <dt>

<span data-ttu-id="4955f-111">*Quelle*</span><span class="sxs-lookup"><span data-stu-id="4955f-111">*Source*</span></span> 
</dt> <dd>

<span data-ttu-id="4955f-112">Ein Zeiger auf die Zeichenfolge, die die Quelle angibt.</span><span class="sxs-lookup"><span data-stu-id="4955f-112">Pointer to the string specifying the source.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4955f-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4955f-113">Return value</span></span>

<span data-ttu-id="4955f-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="4955f-114">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="4955f-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4955f-115">Requirements</span></span>



| <span data-ttu-id="4955f-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4955f-116">Requirement</span></span> | <span data-ttu-id="4955f-117">Wert</span><span class="sxs-lookup"><span data-stu-id="4955f-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4955f-118">Version</span><span class="sxs-lookup"><span data-stu-id="4955f-118">Version</span></span><br/> | <span data-ttu-id="4955f-119">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="4955f-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="4955f-120">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="4955f-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="4955f-121">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="4955f-121">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="4955f-122">DLL</span><span class="sxs-lookup"><span data-stu-id="4955f-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="4955f-123"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4955f-123"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="4955f-124">IID</span><span class="sxs-lookup"><span data-stu-id="4955f-124">IID</span></span><br/>     | <span data-ttu-id="4955f-125">IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="4955f-125">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="4955f-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4955f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4955f-127">**Msisourcelistaddsource**</span><span class="sxs-lookup"><span data-stu-id="4955f-127">**MsiSourceListAddSource**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea)
</dt> <dt>

[<span data-ttu-id="4955f-128">Quellen Resilienz</span><span class="sxs-lookup"><span data-stu-id="4955f-128">source resiliency</span></span>](source-resiliency.md)
</dt> </dl>

 

 




