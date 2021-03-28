---
description: In diesem Thema werden die Konstruktoren der Color-Klasse aufgelistet. Eine komplette Klassen Auflistung finden Sie unter Color-Klasse.
ms.assetid: ebd68c22-9b00-4a8e-9954-e8b0eda764f8
title: Color. Color-Konstruktoren
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 9d6fe2cdc790f87a69395cec5bfadaf653fc8acf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994535"
---
# <a name="colorcolor-constructors"></a><span data-ttu-id="4b15c-104">Color. Color-Konstruktoren</span><span class="sxs-lookup"><span data-stu-id="4b15c-104">Color.Color constructors</span></span>

<span data-ttu-id="4b15c-105">In diesem Thema werden die Konstruktoren der [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) -Klasse aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="4b15c-105">This topic lists the constructors of the [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) class.</span></span> <span data-ttu-id="4b15c-106">Eine komplette Klassen Auflistung finden Sie unter **Color-Klasse**.</span><span class="sxs-lookup"><span data-stu-id="4b15c-106">For a complete class listing, see **Color Class**.</span></span>

### <a name="overload-list"></a><span data-ttu-id="4b15c-107">Überladeliste</span><span class="sxs-lookup"><span data-stu-id="4b15c-107">Overload list</span></span>



| <span data-ttu-id="4b15c-108">Konstruktor</span><span class="sxs-lookup"><span data-stu-id="4b15c-108">Constructor</span></span>                                                               | <span data-ttu-id="4b15c-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4b15c-109">Description</span></span>                                                                                                                                                                                                         |
|:--------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b15c-110">[**Farbe (ARGB)**](/windows/win32/api/gdipluscolor/nf-gdipluscolor-color-color(inargb))</span><span class="sxs-lookup"><span data-stu-id="4b15c-110">[**Color(ARGB)**](/windows/win32/api/gdipluscolor/nf-gdipluscolor-color-color(inargb))</span></span>                   | <span data-ttu-id="4b15c-111">Erstellt ein [**Color:: Color**](/windows/win32/api/gdipluscolor/nf-gdipluscolor-color-color(inargb)) -Objekt mit einem **ARGB** -Wert.</span><span class="sxs-lookup"><span data-stu-id="4b15c-111">Creates a [**Color::Color**](/windows/win32/api/gdipluscolor/nf-gdipluscolor-color-color(inargb)) object by using an **ARGB** value.</span></span><br/>                                                                                                    |
| <span data-ttu-id="4b15c-112">[**Farbe (Byte, Byte, Byte)**](/windows/win32/api/gdipluscolor/nf-gdipluscolor-color-color(inbyte_inbyte_inbyte))</span><span class="sxs-lookup"><span data-stu-id="4b15c-112">[**Color(BYTE,BYTE,BYTE)**](/windows/win32/api/gdipluscolor/nf-gdipluscolor-color-color(inbyte_inbyte_inbyte))</span></span>        | <span data-ttu-id="4b15c-113">Erstellt mithilfe der angegebenen Werte für die roten, grünen und blauen Komponenten ein [**Color:: Color**](/windows/win32/api/gdipluscolor/nf-gdipluscolor-color-color(inbyte_inbyte_inbyte)) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="4b15c-113">Creates a [**Color::Color**](/windows/win32/api/gdipluscolor/nf-gdipluscolor-color-color(inbyte_inbyte_inbyte)) object by using specified values for the red, green, and blue components.</span></span> <span data-ttu-id="4b15c-114">Dieser Konstruktor legt die Alpha Komponente auf 255 (nicht transparent) fest.</span><span class="sxs-lookup"><span data-stu-id="4b15c-114">This constructor sets the alpha component to 255 (opaque).</span></span><br/> |
| <span data-ttu-id="4b15c-115">[**Farbe (Byte, Byte, Byte, Byte)**](/windows/win32/api/gdipluscolor/nf-gdipluscolor-color-color(inbyte_inbyte_inbyte_inbyte))</span><span class="sxs-lookup"><span data-stu-id="4b15c-115">[**Color(BYTE,BYTE,BYTE,BYTE)**](/windows/win32/api/gdipluscolor/nf-gdipluscolor-color-color(inbyte_inbyte_inbyte_inbyte))</span></span> | <span data-ttu-id="4b15c-116">Erstellt mit den angegebenen Werten für die Alpha-, rot-, grün-und Blau-Komponenten ein [**Color:: Color**](/windows/win32/api/gdipluscolor/nf-gdipluscolor-color-color(inbyte_inbyte_inbyte_inbyte)) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="4b15c-116">Creates a [**Color::Color**](/windows/win32/api/gdipluscolor/nf-gdipluscolor-color-color(inbyte_inbyte_inbyte_inbyte)) object by using specified values for the alpha, red, green, and blue components.</span></span><br/>                                                   |
| [<span data-ttu-id="4b15c-117">**Farbe ()**</span><span class="sxs-lookup"><span data-stu-id="4b15c-117">**Color()**</span></span>](/windows/win32/api/gdipluscolor/nf-gdipluscolor-color-color)                            | <span data-ttu-id="4b15c-118">Erstellt ein [**Color:: Color**](/windows/win32/api/gdipluscolor/nf-gdipluscolor-color-color) -Objekt und initialisiert es mit undurchsichtigem schwarz.</span><span class="sxs-lookup"><span data-stu-id="4b15c-118">Creates a [**Color::Color**](/windows/win32/api/gdipluscolor/nf-gdipluscolor-color-color) object and initializes it to opaque black.</span></span> <span data-ttu-id="4b15c-119">Dies ist der Standardkonstruktor</span><span class="sxs-lookup"><span data-stu-id="4b15c-119">This is the default constructor.</span></span><br/>                                                                |



 

 
