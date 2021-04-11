---
description: Bestimmte Werte, die mit konfigurierbaren Mergemodulen verwendet werden, erfordern spezielle Textverarbeitung.
ms.assetid: b9d41400-f3b5-4f85-8728-56f9b90a50ca
title: Spezielles cmsm-Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae9b6fa0bc5e84f125d0872a2937db7701f70820
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215364"
---
# <a name="cmsm-special-format"></a><span data-ttu-id="8fbe4-103">Spezielles cmsm-Format</span><span class="sxs-lookup"><span data-stu-id="8fbe4-103">CMSM Special Format</span></span>

<span data-ttu-id="8fbe4-104">Bestimmte Werte, die mit konfigurierbaren Mergemodulen verwendet werden, erfordern spezielle Textverarbeitung.</span><span class="sxs-lookup"><span data-stu-id="8fbe4-104">Certain values used with configurable merge modules require special text handling.</span></span> <span data-ttu-id="8fbe4-105">Eine Text Zeichenfolge, die als "cmsm Special Format" bezeichnet wird, behandelt das Semikolon (;) und sind (=) Zeichen als reservierte Zeichen, die vom clientmerge-Tool oder Mergemod.dll verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8fbe4-105">A text string described as being in "CMSM Special Format" treats the semicolon (;) and equals (=) characters as reserved characters used by the client merge tool or Mergemod.dll.</span></span>

<span data-ttu-id="8fbe4-106">Das spezielle cmsm-Format wird derzeit an den folgenden Speicherorten verwendet:</span><span class="sxs-lookup"><span data-stu-id="8fbe4-106">CMSM Special format is currently used in the following locations:</span></span>

-   <span data-ttu-id="8fbe4-107">Die Zeilen Spalte der [ModuleSubstitution-Tabelle](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="8fbe4-107">The Row column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>
-   <span data-ttu-id="8fbe4-108">Die Wert Spalte der [ModuleSubstitution-Tabelle](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="8fbe4-108">The Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>
-   <span data-ttu-id="8fbe4-109">Die ContextData-Spalte der [ModuleConfiguration-Tabelle](moduleconfiguration-table.md) , wenn Bitfield der Wert in der Format-Spalte ist.</span><span class="sxs-lookup"><span data-stu-id="8fbe4-109">The ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md) when Bitfield is the value in the Format column.</span></span>
-   <span data-ttu-id="8fbe4-110">Die ContextData-Spalte der [ModuleConfiguration-Tabelle](moduleconfiguration-table.md) , wenn Text der Wert in der Format-Spalte und Enum der Wert in der Type-Spalte ist.</span><span class="sxs-lookup"><span data-stu-id="8fbe4-110">The ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md) when Text is the value in the Format column and Enum is the value in the Type column.</span></span>
-   <span data-ttu-id="8fbe4-111">Die DefaultValue-Spalte der [ModuleConfiguration-Tabelle](moduleconfiguration-table.md) , wenn key der Wert in der Format-Spalte ist.</span><span class="sxs-lookup"><span data-stu-id="8fbe4-111">The DefaultValue column of the [ModuleConfiguration table](moduleconfiguration-table.md) when Key is the value in the Format column.</span></span>
-   <span data-ttu-id="8fbe4-112">Konfigurierbare Elemente im Schlüsselformat, das von der [**providetextdata-Methode**](configuremodule-providetextdata.md)verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8fbe4-112">Configurable items in the Key format used by the [**ProvideTextData method**](configuremodule-providetextdata.md).</span></span>

<span data-ttu-id="8fbe4-113">Um Literale Semikolons oder Gleichheitszeichen in einen Wert im cmsm-Sonderformat einzugeben, stellen Sie dem Zeichen einen umgekehrten Schrägstrich (" \\ ") voran.</span><span class="sxs-lookup"><span data-stu-id="8fbe4-113">To enter literal semicolons or equal characters into a value in CMSM special format, prefix the character with a backslash character ('\\').</span></span> <span data-ttu-id="8fbe4-114">Ein literaler umgekehrter Schrägstrich kann durch zwei umgekehrte Schrägstriche dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="8fbe4-114">A literal backslash can be represented by two backslashes.</span></span> <span data-ttu-id="8fbe4-115">Ein einzelnes Zeichen, dem ein einzelner umgekehrter Schrägstrich vorangestellt ist, wird in das einzelne Zeichen übersetzt, auch wenn das Zeichen nicht als Escapezeichen erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="8fbe4-115">A single character prefixed by a single backslash is translated into the single character, even if escaping the character is not required.</span></span>

<span data-ttu-id="8fbe4-116">Wenn ein Semikolon oder ein Gleichheitszeichen nicht durch einen umgekehrten Schrägstrich vorangestellt ist, aber nicht über ein definiertes Verhalten im Kontext des Werts verfügt, ist die resultierende Zeichenfolge nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="8fbe4-116">If a semicolon or equals character is not prefixed by a backslash yet does not have a defined behavior in the context of the value, the resulting string is undefined.</span></span> <span data-ttu-id="8fbe4-117">Beispielsweise befindet sich die DefaultValue-Spalte der ModuleConfiguration-Tabelle im cmsm-Sonderformat für alle Schlüsselelemente, da das Semikolon das Spalten Trennzeichen ist.</span><span class="sxs-lookup"><span data-stu-id="8fbe4-117">For example, the DefaultValue column of the ModuleConfiguration table is in CMSM special format for all Key items because the semicolon character is the column delimiter.</span></span> <span data-ttu-id="8fbe4-118">Obwohl das Gleichheitszeichen in dieser Zeichenfolge keine besondere Bedeutung hat, müssen Literale gleich Zeichen in dieser Zeichenfolge weiterhin mit Escapezeichen versehen werden.</span><span class="sxs-lookup"><span data-stu-id="8fbe4-118">Although the equal character has no special meaning in this string, literal equal characters must still be escaped in this string.</span></span>

 

 



