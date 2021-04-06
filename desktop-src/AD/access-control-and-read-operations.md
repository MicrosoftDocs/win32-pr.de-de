---
title: Access Control-und Lesevorgänge
description: Sicherheit ist ein impliziter Filter zum Suchen, Aufzählen von Containern oder zum Lesen von Eigenschaften.
ms.assetid: ee46cbc4-5539-48ce-991f-3ad0429f65ca
ms.tgt_platform: multiple
keywords:
- Access Control-und Lesevorgänge (AD)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6aac8797828dd6322723a95f5e2048f986f1230d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036265"
---
# <a name="access-control-and-read-operations"></a><span data-ttu-id="6fe40-104">Access Control-und Lesevorgänge</span><span class="sxs-lookup"><span data-stu-id="6fe40-104">Access Control and Read Operations</span></span>

<span data-ttu-id="6fe40-105">Sicherheit ist ein impliziter Filter zum Suchen, Aufzählen von Containern oder zum Lesen von Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6fe40-105">Security is an implicit filter for searching, enumerating containers, or reading properties.</span></span> <span data-ttu-id="6fe40-106">Wenn Sie nicht über die erforderlichen Zugriffsrechte verfügen, kann der Versuch, Objekte oder Leseeigenschaften aufzulisten, mit den folgenden Fehlercodes fehlschlagen, auch wenn das Objekt oder die Eigenschaft vorhanden ist:</span><span class="sxs-lookup"><span data-stu-id="6fe40-106">If you do not have the necessary access rights, attempts to list objects or read properties can fail with the following error codes even thought the object or property exists:</span></span>

-   <span data-ttu-id="6fe40-107">**E \_ ADS \_ ungültiges \_ Domänen \_ Objekt**</span><span class="sxs-lookup"><span data-stu-id="6fe40-107">**E\_ADS\_INVALID\_DOMAIN\_OBJECT**</span></span>
-   <span data-ttu-id="6fe40-108">**E \_ ADS- \_ Eigenschaft \_ nicht \_ unterstützt**</span><span class="sxs-lookup"><span data-stu-id="6fe40-108">**E\_ADS\_PROPERTY\_NOT\_SUPPORTED**</span></span>
-   <span data-ttu-id="6fe40-109">**E \_ ADS- \_ Eigenschaft \_ nicht \_ gefunden**</span><span class="sxs-lookup"><span data-stu-id="6fe40-109">**E\_ADS\_PROPERTY\_NOT\_FOUND**</span></span>

<span data-ttu-id="6fe40-110">Beachten Sie, dass ein Aufrufer mit dem **AD \_ right \_ actrl \_ DS \_** -Zugriff auf einen Container die untergeordneten Objekte im Container aufzählen kann.</span><span class="sxs-lookup"><span data-stu-id="6fe40-110">Be aware that a caller with **ADS\_RIGHT\_ACTRL\_DS\_LIST** access to a container can enumerate the child objects in the container.</span></span> <span data-ttu-id="6fe40-111">Der Versuch, auf ein untergeordnetes Objekt zuzugreifen, kann jedoch weiterhin einen Fehler verursachen, z. b. ein **\_ \_ unbekanntes \_ Objekt** , wenn der **Aufrufer keinen Ad \_ right \_ actrl \_ DS- \_ Listen \_ Objekt** Zugriff auf das untergeordnete Objekt hat.</span><span class="sxs-lookup"><span data-stu-id="6fe40-111">But an attempt to access a child object can still fail with an error such as **E\_ADS\_UNKNOWN\_OBJECT** if the caller does not have **ADS\_RIGHT\_ACTRL\_DS\_LIST\_OBJECT** access to the child object.</span></span>

<span data-ttu-id="6fe40-112">Die Auswirkung der Sicherheit auf Lesevorgänge wird nicht notwendigerweise als Fehler dargestellt.</span><span class="sxs-lookup"><span data-stu-id="6fe40-112">The impact of security on read operations is not necessarily manifested as an error.</span></span> <span data-ttu-id="6fe40-113">Beispielsweise kann ein Suchvorgang erfolgreich ausgeführt werden, die Suchergebnisse enthalten jedoch keine Objekte oder Eigenschaften, auf die der Aufrufer keinen Zugriff hat.</span><span class="sxs-lookup"><span data-stu-id="6fe40-113">For example, a search operation can succeed, but the search results do not include objects or properties to which the caller does not have access.</span></span>

 

 




