---
description: Fügt der Auflistung das angegebene Oid-Objekt hinzu.
ms.assetid: 0ae087d6-768a-4538-b834-0f936680de05
title: OIDs. Add-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OIDs.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d2fa007798a0657991ec8e37a7dddc9fb4c95b2c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372126"
---
# <a name="oidsadd-method"></a><span data-ttu-id="413e7-103">OIDs. Add-Methode</span><span class="sxs-lookup"><span data-stu-id="413e7-103">OIDs.Add method</span></span>

<span data-ttu-id="413e7-104">\[Die **Add** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="413e7-104">\[The **Add** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="413e7-105">Verwenden Sie stattdessen die [**OidCollection-Klasse**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) im [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="413e7-105">Instead, use the [**OidCollection Class**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="413e7-106">Die **Add** -Methode fügt der Auflistung das angegebene [**OID**](oid.md) -Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="413e7-106">The **Add** method adds the specified [**OID**](oid.md) object to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="413e7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="413e7-107">Syntax</span></span>


```VB
OIDs.Add( _
  ByVal OID _
)
```



## <a name="parameters"></a><span data-ttu-id="413e7-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="413e7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="413e7-109">*OID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="413e7-109">*OID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="413e7-110">Das [**OID**](oid.md) -Objekt, das der Auflistung hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="413e7-110">The [**OID**](oid.md) object to be added to the collection.</span></span> <span data-ttu-id="413e7-111">Das **OID** -Objekt wird basierend auf dem gepunkteten Wert in sortierter Reihenfolge hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="413e7-111">The **OID** object is added in sorted order based on its dotted value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="413e7-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="413e7-112">Return value</span></span>

<span data-ttu-id="413e7-113">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="413e7-113">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="413e7-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="413e7-114">Requirements</span></span>



| <span data-ttu-id="413e7-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="413e7-115">Requirement</span></span> | <span data-ttu-id="413e7-116">Wert</span><span class="sxs-lookup"><span data-stu-id="413e7-116">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="413e7-117">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="413e7-117">Redistributable</span></span><br/> | <span data-ttu-id="413e7-118">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="413e7-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="413e7-119">DLL</span><span class="sxs-lookup"><span data-stu-id="413e7-119">DLL</span></span><br/>             | <dl> <span data-ttu-id="413e7-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="413e7-120"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
