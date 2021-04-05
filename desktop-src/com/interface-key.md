---
title: Schnittstellenschlüssel
description: Registriert neue Schnittstellen durch Zuordnen eines Schnittstellen namens zu einer Schnittstellen-ID (IID). Es muss ein IID-Unterschlüssel für jede neue Schnittstelle vorhanden sein.
ms.assetid: 2b2b7506-ac42-4bc4-bad5-17be57d6b4f5
keywords:
- COM-Registrierungsschlüssel com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ae31de7af534a58b4973629f2b889f3332047f6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037321"
---
# <a name="interface-key"></a><span data-ttu-id="4873a-105">Schnittstellenschlüssel</span><span class="sxs-lookup"><span data-stu-id="4873a-105">Interface Key</span></span>

<span data-ttu-id="4873a-106">Registriert neue Schnittstellen durch Zuordnen eines Schnittstellen namens zu einer Schnittstellen-ID (IID).</span><span class="sxs-lookup"><span data-stu-id="4873a-106">Registers new interfaces by associating an interface name with an interface ID (IID).</span></span> <span data-ttu-id="4873a-107">Es muss ein IID-Unterschlüssel für jede neue Schnittstelle vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="4873a-107">There must be one IID subkey for each new interface.</span></span>

## <a name="registry-key"></a><span data-ttu-id="4873a-108">Registrierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="4873a-108">Registry Key</span></span>

<span data-ttu-id="4873a-109">**HKEY \_ \_ \\ \\ \\ Schnittstelle der Software Klassen der lokalen Maschine** \\ *{* IID *}*</span><span class="sxs-lookup"><span data-stu-id="4873a-109">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\Interface**\\ *{* IID *}*</span></span>



| <span data-ttu-id="4873a-110">Registrierungswert</span><span class="sxs-lookup"><span data-stu-id="4873a-110">Registry value</span></span>                               | <span data-ttu-id="4873a-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4873a-111">Description</span></span>                                                                                            |
|----------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4873a-112">**Typeinterface wurde**</span><span class="sxs-lookup"><span data-stu-id="4873a-112">**BaseInterface**</span></span>](baseinterface.md)       | <span data-ttu-id="4873a-113">Identifiziert die Schnittstelle, von der die aktuelle Schnittstelle abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="4873a-113">Identifies the interface from which the current interface is derived.</span></span>                                  |
| [<span data-ttu-id="4873a-114">**NumMethods**</span><span class="sxs-lookup"><span data-stu-id="4873a-114">**NumMethods**</span></span>](nummethods.md)             | <span data-ttu-id="4873a-115">Enthält die Anzahl der Methoden in der zugeordneten-Schnittstelle, einschließlich Methoden aus abgeleiteten Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="4873a-115">Contains the number of methods in the associated interface, including methods from derived interfaces.</span></span> |
| [<span data-ttu-id="4873a-116">**Proxystubclsid**</span><span class="sxs-lookup"><span data-stu-id="4873a-116">**ProxyStubClsid**</span></span>](proxystubclsid.md)     | <span data-ttu-id="4873a-117">Ordnet eine IID einer CLSID in 16-Bit-Proxy-DLLs zu.</span><span class="sxs-lookup"><span data-stu-id="4873a-117">Maps an IID to a CLSID in 16-bit proxy DLLs.</span></span>                                                           |
| [<span data-ttu-id="4873a-118">**ProxyStubClsid32**</span><span class="sxs-lookup"><span data-stu-id="4873a-118">**ProxyStubClsid32**</span></span>](proxystubclsid32.md) | <span data-ttu-id="4873a-119">Ordnet eine IID einer CLSID in 32-Bit-Proxy-DLLs zu.</span><span class="sxs-lookup"><span data-stu-id="4873a-119">Maps an IID to a CLSID in 32-bit proxy DLLs.</span></span>                                                           |



 

## <a name="remarks"></a><span data-ttu-id="4873a-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4873a-120">Remarks</span></span>

<span data-ttu-id="4873a-121">Der Schlüssel **HKEY- \_ \_ \\ Software \\ Klassen für lokale Computer** entspricht dem Stamm Schlüssel der **HKEY- \_ Klassen \_** , der für die Kompatibilität mit früheren Versionen von com beibehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="4873a-121">The **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes** key corresponds to the **HKEY\_CLASSES\_ROOT** key, which was retained for compatibility with earlier versions of COM.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4873a-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4873a-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4873a-123">**Berfläche**</span><span class="sxs-lookup"><span data-stu-id="4873a-123">**Interface**</span></span>](interface.md)
</dt> </dl>

 

 




