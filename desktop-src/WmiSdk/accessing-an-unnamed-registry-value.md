---
description: Zugreifen auf einen unbenannten Registrierungs Wert
ms.assetid: 1095da4c-8b9f-4674-9801-f2d25c4f372b
ms.tgt_platform: multiple
title: Zugreifen auf einen unbenannten Registrierungs Wert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92860d240598f0353d1f4c9f41a77306942d272b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352523"
---
# <a name="accessing-an-unnamed-registry-value"></a><span data-ttu-id="75ca1-103">Zugreifen auf einen unbenannten Registrierungs Wert</span><span class="sxs-lookup"><span data-stu-id="75ca1-103">Accessing an Unnamed Registry Value</span></span>

<span data-ttu-id="75ca1-104">Der Standardwert oder unbenannte Wert eines Registrierungsschlüssels wird als (Standard) oder <No Name> im Registrierungs-Editor von regedit angezeigt.</span><span class="sxs-lookup"><span data-stu-id="75ca1-104">The default, or unnamed value of a registry key is shown as (Default) or <No Name> in the Regedit registry editor.</span></span> <span data-ttu-id="75ca1-105">Sie können den System Registrierungs Anbieter verwenden, um auf einen unbenannten Registrierungsschlüssel zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="75ca1-105">You can use the System Registry provider to access an unnamed registry key.</span></span> <span data-ttu-id="75ca1-106">Auf ähnliche Weise können Sie auch den System Registrierungs Anbieter verwenden, um auf bitmapbeschreibungen zuzugreifen, die als unbenannte Werte definiert sind.</span><span class="sxs-lookup"><span data-stu-id="75ca1-106">Similarly, you can also use the System Registry provider to access bitmap descriptions, which are defined as unnamed values.</span></span>

<span data-ttu-id="75ca1-107">Im folgenden Verfahren wird beschrieben, wie ein unbenannter Registrierungs Wert abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="75ca1-107">The following procedure describes how to retrieve an unnamed registry value.</span></span>

<span data-ttu-id="75ca1-108">**So rufen Sie einen unbenannten Registrierungs Wert ab**</span><span class="sxs-lookup"><span data-stu-id="75ca1-108">**To retrieve an unnamed registry value**</span></span>

1.  <span data-ttu-id="75ca1-109">Definieren Sie eine Eigenschaft, und legen Sie den **propertycontext** -Qualifizierer dieser Eigenschaft auf eine leere Zeichenfolge fest.</span><span class="sxs-lookup"><span data-stu-id="75ca1-109">Define a property and set the **PropertyContext** qualifier of that property to an empty string.</span></span>

    <span data-ttu-id="75ca1-110">Im folgenden Codebeispiel wird gezeigt, wie die-Klasse Eigenschaften definiert, die Werte für den Schlüssel enthalten, der vom **ClassContext** -Qualifizierer angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="75ca1-110">The following code example shows how the class defines properties to hold values for the key specified by the **ClassContext** qualifier.</span></span> <span data-ttu-id="75ca1-111">Der Standardwert wird in der **default** -Eigenschaft gespeichert.</span><span class="sxs-lookup"><span data-stu-id="75ca1-111">The default value is stored in the **Default** property.</span></span>

    ``` syntax
    [dynamic, 
     provider("RegProv"), 
     ClassContext("local|hkey_local_machine\\software\\"
     "microsoft\\Active Setup\\Installed Components")]

    class RegTrans{
      [key] String Transports="";
      [PropertyContext("")] String Default;
      [PropertyContext("ComponentId")] String ComponentID;
      [PropertyContext("Locale")] String Locale;
    };
    ```

    <span data-ttu-id="75ca1-112">Der Transport Schlüssel verwendet nicht den unbenannten Wert, sodass die Kompilierung dieser MOF-Datei keinen Wert für die **Standard** Eigenschaft erzeugt, es sei denn, es wird ein Registrierungs Bearbeitungs Tool verwendet, um den unbenannten Wert zu ändern.</span><span class="sxs-lookup"><span data-stu-id="75ca1-112">The Transports key does not use the unnamed value, so compilation of this MOF file does not produce any value for the **Default** property unless a registry editing tool is used to change the unnamed value.</span></span>

2.  <span data-ttu-id="75ca1-113">Definieren Sie für eine Bitmapdatei eine Eigenschaft, und legen Sie den **propertycontext** dieser Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="75ca1-113">For a bitmap file, define a property and set the **PropertyContext** of that property.</span></span>

    <span data-ttu-id="75ca1-114">Im folgenden Codebeispiel wird gezeigt, wie eine Eigenschaft definiert wird.</span><span class="sxs-lookup"><span data-stu-id="75ca1-114">The following code example shows how to define a property.</span></span>

    ```mof
    Local|hkey_classes_root\\.bmp
    ```

    

 

 



