---
title: /backward_compat Schalter
description: Der/Backward \_ Kompatibilitäts-Schalter leitet den Mittel l-Compiler zum Deaktivieren einiger erweiterter Features bei der Erstellung von RPC-/com-stubvorzügen.
ms.assetid: eec0ade7-30a0-44e4-92e9-fb03ff657723
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69b558d01b33b99f7d1d9279f729b923ff58df0f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342043"
---
# <a name="backward_compat-switch"></a><span data-ttu-id="7a972-103">/Backward \_ Kompatibilitäts-Schalter</span><span class="sxs-lookup"><span data-stu-id="7a972-103">/backward\_compat Switch</span></span>

<span data-ttu-id="7a972-104">Der/Backward \_ Kompatibilitäts-Schalter leitet den Mittel l-Compiler zum Deaktivieren einiger erweiterter Features bei der Erstellung von RPC-/com-stubvorzügen.</span><span class="sxs-lookup"><span data-stu-id="7a972-104">The /backward\_compat switch directs the MIDL compiler to turn off some advanced features when generating RPC/COM stubs.</span></span>

``` syntax
midl /backward_compat { maybenull_sizeis | zeroout_alignmentgap | 
     BSTR_byvalue_escaping | string_defaultvalue | signed_wchar_t }
```

## <a name="switch-options"></a><span data-ttu-id="7a972-105">Optionen wechseln</span><span class="sxs-lookup"><span data-stu-id="7a972-105">Switch Options</span></span>

<span data-ttu-id="7a972-106">*maybenull \_ sizeis*</span><span class="sxs-lookup"><span data-stu-id="7a972-106">*maybenull\_sizeis*</span></span><dl> <span data-ttu-id="7a972-107">Wendet das Attribut " [ \[ \_ Konsistenz \_ Prüfung \] Deaktivieren](disable-consistence-check.md) " auf eine gesamte Mittell-Kompilierung an.</span><span class="sxs-lookup"><span data-stu-id="7a972-107">Applies the [\[disable\_consistency\_check\]](disable-consistence-check.md) attribute to an entire MIDL compilation.</span></span>  
</dl>

<span data-ttu-id="7a972-108">*NULL ( \_ alignmentgap)*</span><span class="sxs-lookup"><span data-stu-id="7a972-108">*zeroout\_alignmentgap*</span></span><dl> <span data-ttu-id="7a972-109">Deaktiviert das nulren von Lücken im gemarshallten Puffer.</span><span class="sxs-lookup"><span data-stu-id="7a972-109">Turns off zeroing out gaps in the marshaled buffer.</span></span>  
</dl>

<span data-ttu-id="7a972-110">*BSTR byvalue-Escapezeichen \_ \_*</span><span class="sxs-lookup"><span data-stu-id="7a972-110">*BSTR\_byvalue\_escaping*</span></span><dl> <span data-ttu-id="7a972-111">Weist den Mittel l-Compiler an, Escapesequenzen zu berücksichtigen, z \\ . b.-™ oder- \\ ™ in bstrins.</span><span class="sxs-lookup"><span data-stu-id="7a972-111">Directs the MIDL compiler to honor escape sequences such as â€˜\\nâ€™ or â€˜\\tâ€™ in BSTRs.</span></span>  
</dl>

<span data-ttu-id="7a972-112">*String \_ DefaultValue*</span><span class="sxs-lookup"><span data-stu-id="7a972-112">*string\_defaultvalue*</span></span><dl> <span data-ttu-id="7a972-113">Erzwingt, dass der mittlerer l-Compiler Zeichen folgen in [**\[ DefaultValue \]**](defaultvalue.md) -Attributen in Variant umwandelt. VT \_ I4 geben Sie ein, bevor Sie den Wert in den richtigen Typ umwandeln.</span><span class="sxs-lookup"><span data-stu-id="7a972-113">Forces the MIDL compiler to coerce strings in [**\[defaultvalue\]**](defaultvalue.md) attributes into VARIANT.VT\_I4 type before coercing the value into the correct type.</span></span>  
</dl>

<span data-ttu-id="7a972-114">*signiertes \_ WCHAR \_ t*</span><span class="sxs-lookup"><span data-stu-id="7a972-114">*signed\_wchar\_t*</span></span><dl> <span data-ttu-id="7a972-115">Leitet die Mittell so um, dass der WCHAR \_ t-Typ für die Kompatibilität mit Visual Basic als signiert behandelt wird.</span><span class="sxs-lookup"><span data-stu-id="7a972-115">Directs MIDL to treat the wchar\_t type as signed for compatibility with Visual Basic.</span></span>  
</dl>

## <a name="remarks"></a><span data-ttu-id="7a972-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7a972-116">Remarks</span></span>

-   <span data-ttu-id="7a972-117">*maybenull \_ sizeis*: siehe \[ Deaktivieren der \_ Konsistenz \_ Prüfung \] .</span><span class="sxs-lookup"><span data-stu-id="7a972-117">*maybenull\_sizeis*: See \[disable\_consistency\_check\].</span></span>
-   <span data-ttu-id="7a972-118">*Nullen von \_ alignmentgap*: Wenn IDLs mit "target nt60" oder höher kompiliert werden, erstellt die Mittel-l stubwerte, die alle Ausrichtungs Lücken zwischen Membern oder einer Struktur im Wire-Puffer Nullen.</span><span class="sxs-lookup"><span data-stu-id="7a972-118">*zeroout\_alignmentgap*: When IDLs are compiled with â€“target NT60 or higher, MIDL will create stubs that zero out any alignment gaps between members or a structure in the wire buffer.</span></span> <span data-ttu-id="7a972-119">Der Befehls Zeilenschalter */Backward \_ Kompatibilitäts ZeroOut \_ alignmentgap* leitet "Mittel l" ein, um diese Funktion zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="7a972-119">The command line switch */backward\_compat zeroout\_alignmentgap* directs MIDL to disable this feature.</span></span>

    <span data-ttu-id="7a972-120">In der folgenden Beispiel Struktur enthält der Wire-Puffer eine Ausrichtungs Lücke von 7 Byte, um den Hyper-Member nach dem char-Member auf 8 auszurichten.</span><span class="sxs-lookup"><span data-stu-id="7a972-120">In the following example structure, the wire buffer contains a 7 byte alignment gap to align the hyper member to 8 after the char member.</span></span> <span data-ttu-id="7a972-121">Bei Verwendung von "target nt60" oder höher wird diese Lücke von mittlerer l außer 0 gesetzt, es sei denn, es wird der Schalter verwendet.</span><span class="sxs-lookup"><span data-stu-id="7a972-121">With â€“target NT60 or higher, MIDL will zero out that gap unless the switch is used.</span></span>

    <span data-ttu-id="7a972-122">IDL-Datei:</span><span class="sxs-lookup"><span data-stu-id="7a972-122">IDL file:</span></span>

    ``` syntax
    typedef struct _structwithgaps{
        char c;
        // 7 byte gap to align the following hyper to 8 
        hyper h;
    } structwithgap;
    ```

    <span data-ttu-id="7a972-123">Dieser Switch kann eine geringfügige Leistungsverbesserung mit potenziell erheblichen Erhöhung der Offenlegung von Risiken bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="7a972-123">This switch can provide a slight performance improvement with potentially significant increases in disclosure risk.</span></span>

-   <span data-ttu-id="7a972-124">*BSTR- \_ byvalue \_*-Escapezeichen: der Interl-Compiler verarbeitet standardmäßig keine Escapesequenzen, wie™ z. b., d \\ \\ . b.™ in Zeichen folgen Konstanten für die OLE-Automatisierung, wenn eine Zeichen folgen Konstante in die Typen VT \_ LPSTR oder VT \_ LPWSTR geändert wird.</span><span class="sxs-lookup"><span data-stu-id="7a972-124">*BSTR\_byvalue\_escaping*: By default, the MIDL compiler does not process escape sequences such as â€˜\\nâ€™ or â€˜\\tâ€™ in string constants for OLE Automation when converting a string constant to types VT\_LPSTR or VT\_LPWSTR.</span></span> <span data-ttu-id="7a972-125">Mit dieser Option für die Abwärtskompatibilität werden die Escapesequenzen ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="7a972-125">With this backward compatibility switch option, the escape sequences are evaluated.</span></span>
-   <span data-ttu-id="7a972-126">*String \_ DefaultValue*: erzwingt, dass der mittlerer l-Compiler numerische Zeichen folgen in [**\[ DefaultValue \]**](defaultvalue.md) -Attributen in Variant umwandelt. VT \_ I4 geben Sie ein, bevor Sie den Wert in den richtigen Typ umwandeln.</span><span class="sxs-lookup"><span data-stu-id="7a972-126">*string\_defaultvalue*: Forces the MIDL compiler to coerce numeric strings in [**\[defaultvalue\]**](defaultvalue.md) attributes into VARIANT.VT\_I4 type before coercing the value into the correct type.</span></span> <span data-ttu-id="7a972-127">Dies kann in einigen Fällen zu einem Genauigkeits Verlust führen, daher wird diese Switch-Option nicht empfohlen.</span><span class="sxs-lookup"><span data-stu-id="7a972-127">This can lead to loss of precision in some cases, so this switch option is not recommended.</span></span>
-   <span data-ttu-id="7a972-128">*signiertes \_ WCHAR \_ t*: leitet die mittlere Zahl so um, dass der WCHAR \_ t-Typ für die Kompatibilität mit Visual Basic als signiert behandelt wird.</span><span class="sxs-lookup"><span data-stu-id="7a972-128">*signed\_wchar\_t*: Directs MIDL to treat the wchar\_t type as signed for compatibility with Visual Basic.</span></span>

 

 




