---
description: Die collectuserinfo-Methode des Installer-Objekts Ruft eine Assistenten Sequenz für eine Benutzeroberfläche auf, die sowohl Benutzerinformationen als auch den Produktcode sammelt und speichert.
ms.assetid: 2faacf38-1af1-4e8a-a3f6-87733104614e
title: Installer. collectuserinfo-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.CollectUserInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d7286fdbc9fab6b3db6752284bf86db05f920bd7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370159"
---
# <a name="installercollectuserinfo-method"></a><span data-ttu-id="3c982-103">Installer. collectuserinfo-Methode</span><span class="sxs-lookup"><span data-stu-id="3c982-103">Installer.CollectUserInfo method</span></span>

<span data-ttu-id="3c982-104">Die **collectuserinfo** -Methode des [**Installer**](installer-object.md) -Objekts Ruft eine Assistenten Sequenz für eine Benutzeroberfläche auf, die sowohl Benutzerinformationen als auch den Produktcode sammelt und speichert.</span><span class="sxs-lookup"><span data-stu-id="3c982-104">The **CollectUserInfo** method of the [**Installer**](installer-object.md) object invokes a user interface wizard sequence which collects and stores both user information and the product code.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c982-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3c982-105">Syntax</span></span>


```JScript
Installer.CollectUserInfo(
  Product
)
```



## <a name="parameters"></a><span data-ttu-id="3c982-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3c982-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c982-107">*Produkt*</span><span class="sxs-lookup"><span data-stu-id="3c982-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="3c982-108">Gibt den [**Produktcode**](productcode.md) des Produkts an.</span><span class="sxs-lookup"><span data-stu-id="3c982-108">Specifies the [**product code**](productcode.md) of the product.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c982-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3c982-109">Return value</span></span>

<span data-ttu-id="3c982-110">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="3c982-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c982-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3c982-111">Remarks</span></span>

<span data-ttu-id="3c982-112">Eine Anwendung sollte die Methode **collectuserinfo** beim ersten Ausführen aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="3c982-112">An application should call the **CollectUserInfo** method the first time it is run.</span></span> <span data-ttu-id="3c982-113">Mit der **collectuserinfo** -Methode wird das Installationspaket des Produkts geöffnet, und es wird eine erstellte Assistenten Sequenz aufgerufen, die Benutzerinformationen sammelt.</span><span class="sxs-lookup"><span data-stu-id="3c982-113">The **CollectUserInfo** method opens the product's installation package and invokes an authored user interface wizard sequence which collects user information.</span></span> <span data-ttu-id="3c982-114">Nach Abschluss der Assistenten Sequenz werden die gesammelten Benutzerinformationen registriert.</span><span class="sxs-lookup"><span data-stu-id="3c982-114">Upon completion of the wizard sequence, the collected user information is registered.</span></span> <span data-ttu-id="3c982-115">Die [**uilevel**](installer-uilevel.md) -Eigenschaft sollte auf msiuilevelfull festgelegt werden, da diese API eine erstellte Benutzeroberfläche erfordert.</span><span class="sxs-lookup"><span data-stu-id="3c982-115">The [**UILevel**](installer-uilevel.md) property should be set to msiUILevelFull because this API requires an authored user interface.</span></span>

<span data-ttu-id="3c982-116">Die **collectuserinfo** -Methode ruft das [FIRSTRUN-Dialog](firstrun-dialog.md)Feld auf.</span><span class="sxs-lookup"><span data-stu-id="3c982-116">The **CollectUserInfo** method invokes the [FirstRun Dialog](firstrun-dialog.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3c982-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3c982-117">Requirements</span></span>



| <span data-ttu-id="3c982-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3c982-118">Requirement</span></span> | <span data-ttu-id="3c982-119">Wert</span><span class="sxs-lookup"><span data-stu-id="3c982-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c982-120">Version</span><span class="sxs-lookup"><span data-stu-id="3c982-120">Version</span></span><br/> | <span data-ttu-id="3c982-121">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3c982-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="3c982-122">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3c982-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="3c982-123">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="3c982-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="3c982-124">DLL</span><span class="sxs-lookup"><span data-stu-id="3c982-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="3c982-125"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c982-125"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="3c982-126">IID</span><span class="sxs-lookup"><span data-stu-id="3c982-126">IID</span></span><br/>     | <span data-ttu-id="3c982-127">IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="3c982-127">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="3c982-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3c982-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c982-129">**Msicollectuserinfo**</span><span class="sxs-lookup"><span data-stu-id="3c982-129">**MsiCollectUserInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa)
</dt> </dl>

 

 




