---
title: Verwenden von ACF-Attributen in einer IDL-Datei
description: Sie können die \_ MIDL-Compileroption /app config verwenden, um Bindungshandleattribute in der IDL-Datei anstelle einer separaten ACF-Datei anzugeben.
ms.assetid: 3558e818-b39f-42a4-842f-05970296da0e
keywords:
- ACF MIDL , Attribute, verwenden ACF in IDL
- IDL MIDL mit ACF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bda925a3b3242072f297c8828427ae4f7a488d1f3b002e05ace6bec45a46d2d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105520"
---
# <a name="using-acf-attributes-in-an-idl-file"></a>Verwenden von ACF-Attributen in einer IDL-Datei

Sie können die MIDL-Compileroption [**/app \_ config**](-app-config.md) verwenden, um Bindungshandleattribute in der IDL-Datei anstelle einer separaten ACF-Datei anzugeben. Insbesondere können Sie die Attribute für das [**automatische \_ Handle,**](auto-handle.md)das [**implizite \_ Handle**](implicit-handle.md)und das [**explizite \_ Handle**](explicit-handle.md) auf den Header einer RPC-Schnittstelle in einer IDL-Datei anwenden. Verwenden Sie diese Option, wenn Ihre RPC-Anwendung keine anderen ACF-Attribute erfordert und sie keine strikte OSF-DCE-Kompatibilität erfordert.

 

 




