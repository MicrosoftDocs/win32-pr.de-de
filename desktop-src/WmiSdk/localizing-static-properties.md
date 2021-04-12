---
description: Sie können statische Eigenschaften mithilfe von partiellen Wert Maps lokalisieren.
ms.assetid: 67e91454-c065-4ab2-a373-245c9392c71c
ms.tgt_platform: multiple
title: Lokalisieren statischer Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecaba200b7880991d349c6e0c0196c88ffa54b11
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "104356166"
---
# <a name="localizing-static-properties"></a><span data-ttu-id="3657c-103">Lokalisieren statischer Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3657c-103">Localizing Static Properties</span></span>

<span data-ttu-id="3657c-104">Sie können statische Eigenschaften mithilfe von partiellen Wert Maps lokalisieren.</span><span class="sxs-lookup"><span data-stu-id="3657c-104">You can localize static properties by using partial value maps.</span></span>

<span data-ttu-id="3657c-105">Im folgenden Verfahren wird beschrieben, wie statische Eigenschaften mithilfe von partiellen Wert Maps mit regulären Ausdrücken lokalisiert werden können.</span><span class="sxs-lookup"><span data-stu-id="3657c-105">The following procedure describes how static properties can be localized using partial value maps with regular expressions.</span></span>

<span data-ttu-id="3657c-106">**So verwenden Sie Werte Zuordnungen zum Lokalisieren statischer Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="3657c-106">**To use value maps to localize static properties**</span></span>

1.  <span data-ttu-id="3657c-107">Erstellen Sie eine MOF-Master Datei (mastervm. MOF).</span><span class="sxs-lookup"><span data-stu-id="3657c-107">Create a master MOF file (Mastervm.mof).</span></span>

    <span data-ttu-id="3657c-108">Das folgende Codebeispiel kann verwendet werden, um eine MOF-Master Datei (mastervm. MOF) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3657c-108">The following code example can be used to create a master MOF file (Mastervm.mof).</span></span>

    ```syntax
    [Locale(0x409)]
    class Group1
    {
        [key] string ID;
        [DisplayName("Numbers"),
            ValueMap{0,1,2,3}:amended,
            Values{"Zero", "One", "Two", "Three"}:amended]
        Uint32 Numbers;
    };
    ```

2.  <span data-ttu-id="3657c-109">Erstellen Sie sprachneutrale und sprachspezifische Versionen der MOF-Datei.</span><span class="sxs-lookup"><span data-stu-id="3657c-109">Create the language-neutral and language-specific versions of the MOF file.</span></span>

    <span data-ttu-id="3657c-110">Geben Sie den folgenden Befehl an einer Eingabeaufforderung ein, um die sprach neutralen und sprachspezifischen Versionen der MOF-Datei zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3657c-110">Type the following command at a command prompt to create the language-neutral and language-specific versions of the MOF file.</span></span>

    ```syntax
    mofcomp -MOF:LnVm.mof -MFL:LsVm.mfl -Amendment:MS_409 MasterVm.mof
    ```

    <span data-ttu-id="3657c-111">Der MOF-Compiler generiert die sprachspezifischen und sprach neutralen MOF-Dateien lnvm. mof und lsvm. MFL.</span><span class="sxs-lookup"><span data-stu-id="3657c-111">The MOF compiler generates the language-specific and language-neutral MOF files, LnVm.mof and LsVm.mfl.</span></span> <span data-ttu-id="3657c-112">Die American English-Werte für die [Numbers](numbers.md) -Eigenschaft befinden sich in der MFL-Datei für den American English-Namespace.</span><span class="sxs-lookup"><span data-stu-id="3657c-112">The American English values for the [Numbers](numbers.md) property is placed in the .mfl file for the American English namespace.</span></span>

    <span data-ttu-id="3657c-113">Im folgenden Codebeispiel wird der Inhalt der Datei "lsvm. MFL" veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="3657c-113">The following code example shows the contents of the LsVm.mfl file.</span></span>

    ```syntax
    #pragma namespace("\\\\.\\root\\default")
    instance of __namespace{ name="ms_409";};
    #pragma namespace("\\\\.\\root\\default\\ms_409")

    [AMENDMENT, LOCALE(0x409)] 
    class Group1
    {
      [ValueMap{0, 1, 2, 3} : Amended,
          Values{"Zero", "One", "Two", "Three"} : Amended] 
      Uint32 Numbers;
    };
    ```

3.  <span data-ttu-id="3657c-114">Kompilieren Sie die beiden MOF-Dateien, und speichern Sie die Klassen Informationen im CIM-Repository.</span><span class="sxs-lookup"><span data-stu-id="3657c-114">Compile the two MOF files and store the class information in the CIM repository.</span></span>

    <span data-ttu-id="3657c-115">Geben Sie den folgenden Befehl an einer Eingabeaufforderung ein, um die beiden MOF-Dateien zu kompilieren.</span><span class="sxs-lookup"><span data-stu-id="3657c-115">Type the following command at a command prompt to compile the two MOF files.</span></span>

    ```syntax
    Mofcomp LnVm.mof 
    Mofcomp LsVm.mfl
    ```

4.  <span data-ttu-id="3657c-116">Lokalisieren Sie die MFL-Datei für andere Gebiets Schemas.</span><span class="sxs-lookup"><span data-stu-id="3657c-116">Localize the MFL file for other locales.</span></span>

    <span data-ttu-id="3657c-117">Das folgende Codebeispiel zeigt den Inhalt einer MFL-Datei für den französischen Namespace.</span><span class="sxs-lookup"><span data-stu-id="3657c-117">The following code example shows the contents of an MFL file for the French namespace.</span></span>

    ```syntax
    #pragma namespace("\\\\.\\root\\default")
    instance of __namespace{ name="ms_40C";};
    #pragma namespace("\\\\.\\root\\default\\ms_40C")

    [AMENDMENT, LOCALE(0x40C)] 
    class Group1
    {
        [key] string ID;
        [ValueMap{0, 1, 2, 3} : Amended,
            Values{"Zero", "Un", "Deux", "Trois"} : Amended]
        Uint32 Numbers;
    };
    ```

<span data-ttu-id="3657c-118">Das Ergebnis ist, dass sowohl der Anzeige Name als auch der Wert der [Numbers](numbers.md) -Eigenschaft vom Gebiets Schema des angemeldeten Benutzers abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="3657c-118">The net result is that both the display name and the value of the [Numbers](numbers.md) property depend on the locale of the logged-on user.</span></span> <span data-ttu-id="3657c-119">Wenn der Benutzer ein nicht bereitgestelltes Gebiets Schema angibt, stammen die Standard qualifiziererdaten aus dem englischen \_ Namespace (MS 409).</span><span class="sxs-lookup"><span data-stu-id="3657c-119">If the user specifies a locale that has not been provided, the default qualifier data comes from the English (ms\_409) namespace.</span></span>

<span data-ttu-id="3657c-120">Die Auswirkung dieses Entwurfs ist, dass jeder Zeichen folgen Wert als Such Bezeichner verwendet wird, der nicht lokalisiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="3657c-120">The implication of this design is that each string value is used as a lookup identifier, which cannot be localized.</span></span> <span data-ttu-id="3657c-121">Wenn Sie dieses Schema definieren, müssen Sie sicherstellen, dass der Wert, den der Anbieter einfügt, Gebiets Schema unabhängig ist.</span><span class="sxs-lookup"><span data-stu-id="3657c-121">When defining this scheme, you must ensure that the value the provider puts in is locale-independent.</span></span>

> [!Note]  
> <span data-ttu-id="3657c-122">WMI bietet derzeit keine Laufzeitunterstützung für die Zuordnung von Werten zu Zeichen folgen, die von Qualifizierern definiert werden.</span><span class="sxs-lookup"><span data-stu-id="3657c-122">WMI does not currently provide run-time support for mapping values to strings defined by qualifiers.</span></span> <span data-ttu-id="3657c-123">Die Interpretation der empfohlenen Syntax ist die Zuständigkeit der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="3657c-123">Interpretation of the suggested syntax is the application's responsibility.</span></span>

 

 

 



