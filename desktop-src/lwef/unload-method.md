---
title: Unload-Methode
description: Unload-Methode
ms.assetid: 2ffaeea6-ff24-48b2-bc99-eba429434a30
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41d19f5f29647ff01b5a52bd8978694aaef1c43a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725913"
---
# <a name="unload-method"></a><span data-ttu-id="84233-103">Unload-Methode</span><span class="sxs-lookup"><span data-stu-id="84233-103">Unload Method</span></span>

<span data-ttu-id="84233-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="84233-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="84233-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="84233-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="84233-106">Entlädt die Zeichendaten für das angegebene Zeichen.</span><span class="sxs-lookup"><span data-stu-id="84233-106">Unloads the character data for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="84233-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="84233-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="84233-108">*Agent ***. Zeichen. entladen "*** Merkmal-ID \* *"**</span><span class="sxs-lookup"><span data-stu-id="84233-108">*agent ***.Characters.Unload "*** CharacterID\*\*\*"*\*</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="84233-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="84233-109">Remarks</span></span>

<span data-ttu-id="84233-110">Verwenden Sie diese Methode, wenn Sie kein Zeichen mehr benötigen, um Arbeitsspeicher freizugeben, der zum Speichern von Informationen über das Zeichen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="84233-110">Use this method when you no longer need a character, to free up memory used to store information about the character.</span></span> <span data-ttu-id="84233-111">Wenn Sie erneut auf das Zeichen zugreifen, verwenden Sie die [**Load**](load-method.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="84233-111">If you access the character again, use the [**Load**](load-method.md) method.</span></span>

<span data-ttu-id="84233-112">Diese Methode gibt kein [**Anforderungs**](/windows/desktop/lwef/the-request-object) Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="84233-112">This method does not return a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span>

 

 