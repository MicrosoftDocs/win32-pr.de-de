---
description: Die dvdadm-Eigenschaft ermöglicht den Zugriff auf das msdvdadm-Objekt, das Methoden und Eigenschaften zum Speichern von Anwendungs-und Benutzerinformationen enthält.
ms.assetid: eb73a851-7118-42f3-be99-1cf356d2e37a
title: Dvdadm (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c3d81742fc6e643d6ee805a76c14d07d45d1924
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124585"
---
# <a name="dvdadm-property"></a><span data-ttu-id="f3bfc-103">Dvdadm (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f3bfc-103">DVDAdm Property</span></span>

> [!Note]  
> <span data-ttu-id="f3bfc-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f3bfc-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="f3bfc-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="f3bfc-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="f3bfc-106">Die- `DVDAdm` Eigenschaft ermöglicht den Zugriff auf das [msdvdadm](msdvdadm-object.md) -Objekt, das Methoden und Eigenschaften zum Speichern von Anwendungs-und Benutzerinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="f3bfc-106">The `DVDAdm` property provides access to the [MSDVDAdm](msdvdadm-object.md) object that contains methods and properties for saving application and user information.</span></span>

``` syntax
        MSWebDVD.DVDAdm
```

## <a name="remarks"></a><span data-ttu-id="f3bfc-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f3bfc-107">Remarks</span></span>

<span data-ttu-id="f3bfc-108">Diese Eigenschaft ist schreibgeschützt und weist keinen Standardwert auf.</span><span class="sxs-lookup"><span data-stu-id="f3bfc-108">This property is read-only with no default value.</span></span> <span data-ttu-id="f3bfc-109">Es ist nicht erforderlich, einen separaten Verweis auf das **msdvdadm** -Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f3bfc-109">There is no need to create a separate reference to the **MSDVDAdm** object.</span></span> <span data-ttu-id="f3bfc-110">Um auf die Methoden und Eigenschaften des-Objekts zuzugreifen, verwenden Sie die- `DVDAdm` Eigenschaft, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="f3bfc-110">To access the methods and properties of the object, use the `DVDAdm` property as shown in the following example.</span></span>

## <a name="examples"></a><span data-ttu-id="f3bfc-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f3bfc-111">Examples</span></span>


```VB
DVD.DVDAdm.DisableScreenSaver = true
```



 

 



