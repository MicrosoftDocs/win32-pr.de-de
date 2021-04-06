---
title: Verwenden von ACF-Attributen in einer IDL-Datei
description: Mit der/app config- \_ Compileroption können Sie Bindungs handle-Attribute in der IDL-Datei anstelle einer separaten ACF-Datei angeben.
ms.assetid: 3558e818-b39f-42a4-842f-05970296da0e
keywords:
- ACF-Mittell, Attribute, verwenden von ACF in IDL
- IDL-Mittell, Verwendung von ACF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 712dde95201bc2c729ac126b35e04919fd196cbb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709815"
---
# <a name="using-acf-attributes-in-an-idl-file"></a><span data-ttu-id="e35c8-105">Verwenden von ACF-Attributen in einer IDL-Datei</span><span class="sxs-lookup"><span data-stu-id="e35c8-105">Using ACF Attributes in an IDL File</span></span>

<span data-ttu-id="e35c8-106">Sie können die kompil-Compileroption/[**App \_ config**](-app-config.md) verwenden, um Bindungs handle-Attribute in der IDL-Datei anstelle einer separaten ACF-Datei anzugeben.</span><span class="sxs-lookup"><span data-stu-id="e35c8-106">You can use the /[**app\_config**](-app-config.md) MIDL compiler option to specify binding handle attributes in the IDL file rather than in a separate ACF file.</span></span> <span data-ttu-id="e35c8-107">Insbesondere können Sie das [**Auto \_ handle**](auto-handle.md), das [**implizite \_ handle**](implicit-handle.md)und [**explizite \_ handle**](explicit-handle.md) -Attribute auf den Header einer RPC-Schnittstelle in einer IDL-Datei anwenden.</span><span class="sxs-lookup"><span data-stu-id="e35c8-107">Specifically, you can apply the [**auto\_handle**](auto-handle.md), [**implicit\_handle**](implicit-handle.md), and [**explicit\_handle**](explicit-handle.md) attributes to the header of an RPC interface in an IDL file.</span></span> <span data-ttu-id="e35c8-108">Verwenden Sie diese Option, wenn Ihre RPC-Anwendung keine anderen ACF-Attribute erfordert, und wenn Sie keine strikte OSF-DCE-Kompatibilität benötigen.</span><span class="sxs-lookup"><span data-stu-id="e35c8-108">Consider using this option if your RPC application does not require other ACF attributes, and if you do not require strict OSF-DCE compatibility.</span></span>

 

 




