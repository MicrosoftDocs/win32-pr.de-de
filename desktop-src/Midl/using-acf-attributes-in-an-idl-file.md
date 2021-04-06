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
# <a name="using-acf-attributes-in-an-idl-file"></a>Verwenden von ACF-Attributen in einer IDL-Datei

Sie können die kompil-Compileroption/[**App \_ config**](-app-config.md) verwenden, um Bindungs handle-Attribute in der IDL-Datei anstelle einer separaten ACF-Datei anzugeben. Insbesondere können Sie das [**Auto \_ handle**](auto-handle.md), das [**implizite \_ handle**](implicit-handle.md)und [**explizite \_ handle**](explicit-handle.md) -Attribute auf den Header einer RPC-Schnittstelle in einer IDL-Datei anwenden. Verwenden Sie diese Option, wenn Ihre RPC-Anwendung keine anderen ACF-Attribute erfordert, und wenn Sie keine strikte OSF-DCE-Kompatibilität benötigen.

 

 




