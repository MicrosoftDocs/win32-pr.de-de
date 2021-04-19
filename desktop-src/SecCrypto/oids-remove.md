---
description: Entfernt das angegebene Oid-Objekt aus der Auflistung.
ms.assetid: c5eb6831-b195-4dc1-a6bd-d4245f9b0213
title: OIDs. Remove-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OIDs.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 000310e0034d413dea16a45f79647c3e0f7cf52d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106350790"
---
# <a name="oidsremove-method"></a><span data-ttu-id="ca367-103">OIDs. Remove-Methode</span><span class="sxs-lookup"><span data-stu-id="ca367-103">OIDs.Remove method</span></span>

<span data-ttu-id="ca367-104">\[Die **Remove** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="ca367-104">\[The **Remove** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ca367-105">Verwenden Sie stattdessen die [**OidCollection-Klasse**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) im [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="ca367-105">Instead, use the [**OidCollection Class**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="ca367-106">Die **Remove** -Methode entfernt das angegebene [**OID**](oid.md) -Objekt aus der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="ca367-106">The **Remove** method removes the specified [**OID**](oid.md) object from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca367-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca367-107">Syntax</span></span>


```VB
OIDs.Remove( _
  ByVal Index _
)
```



## <a name="parameters"></a><span data-ttu-id="ca367-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ca367-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca367-109">*Index* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ca367-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca367-110">Der Index des zu entfernenden [**OID**](oid.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="ca367-110">Index of the [**OID**](oid.md) object to be removed.</span></span> <span data-ttu-id="ca367-111">Dabei kann es sich entweder um einen Index in der Auflistung oder um den gepunkteten Wert der OID handeln.</span><span class="sxs-lookup"><span data-stu-id="ca367-111">This can be either an index into the collection or the dotted value of the OID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca367-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ca367-112">Return value</span></span>

<span data-ttu-id="ca367-113">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ca367-113">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca367-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ca367-114">Requirements</span></span>



| <span data-ttu-id="ca367-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ca367-115">Requirement</span></span> | <span data-ttu-id="ca367-116">Wert</span><span class="sxs-lookup"><span data-stu-id="ca367-116">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ca367-117">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="ca367-117">Redistributable</span></span><br/> | <span data-ttu-id="ca367-118">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="ca367-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="ca367-119">DLL</span><span class="sxs-lookup"><span data-stu-id="ca367-119">DLL</span></span><br/>             | <dl> <span data-ttu-id="ca367-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca367-120"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
