---
description: Gibt ein RecordList-Objekt zurück, das Produkte auflistet, die eine angegebene installierte Komponente verwenden.
ms.assetid: c9756526-68d7-4d04-97e2-56a5eaf816be
title: Installer. clientsex (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ClientsEx
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5a609ab0ba6edc5b0e3e9bbd26bc3539858ebdee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355942"
---
# <a name="installerclientsex-property"></a><span data-ttu-id="89cbe-103">Installer. clientsex (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="89cbe-103">Installer.ClientsEx property</span></span>

<span data-ttu-id="89cbe-104">Diese Eigenschaft gibt ein [**RecordList**](recordlist-object.md) -Objekt zurück, das Produkte auflistet, die eine angegebene installierte Komponente verwenden.</span><span class="sxs-lookup"><span data-stu-id="89cbe-104">This property returns a [**RecordList**](recordlist-object.md) object that lists products that use a specified installed component.</span></span> <span data-ttu-id="89cbe-105">Diese Eigenschaft ruft [**msienumschlag clientsex**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa)auf.</span><span class="sxs-lookup"><span data-stu-id="89cbe-105">This property calls [**MsiEnumClientsEx**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa).</span></span>

<span data-ttu-id="89cbe-106">**[Windows Installer 4,5 oder früher](not-supported-in-windows-installer-4-5.md):** Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="89cbe-106">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="89cbe-107">Diese Eigenschaft ist ab Windows Installer 5,0 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="89cbe-107">This property is available beginning with Windows Installer 5.0.</span></span>

<span data-ttu-id="89cbe-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="89cbe-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="89cbe-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="89cbe-109">Syntax</span></span>


```JScript
propVal = Installer.ClientsEx
```



## <a name="property-value"></a><span data-ttu-id="89cbe-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="89cbe-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="89cbe-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="89cbe-111">Requirements</span></span>



| <span data-ttu-id="89cbe-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="89cbe-112">Requirement</span></span> | <span data-ttu-id="89cbe-113">Wert</span><span class="sxs-lookup"><span data-stu-id="89cbe-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89cbe-114">Version</span><span class="sxs-lookup"><span data-stu-id="89cbe-114">Version</span></span><br/> | <span data-ttu-id="89cbe-115">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7</span><span class="sxs-lookup"><span data-stu-id="89cbe-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7</span></span><br/> |
| <span data-ttu-id="89cbe-116">DLL</span><span class="sxs-lookup"><span data-stu-id="89cbe-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="89cbe-117"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89cbe-117"><dt>Msi.dll</dt></span></span> </dl>                      |
| <span data-ttu-id="89cbe-118">IID</span><span class="sxs-lookup"><span data-stu-id="89cbe-118">IID</span></span><br/>     | <span data-ttu-id="89cbe-119">IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="89cbe-119">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="89cbe-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="89cbe-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89cbe-121">**Msienumschlag clientsex**</span><span class="sxs-lookup"><span data-stu-id="89cbe-121">**MsiEnumClientsEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumclientsexa)
</dt> </dl>

 

 




