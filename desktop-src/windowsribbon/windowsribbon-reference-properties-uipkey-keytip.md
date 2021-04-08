---
title: UI_PKEY_Keytip
description: Bezeichnet die Benutzeroberflächen- \_ pkey- \_ KeyTip-Eigenschaft.
ms.assetid: 7af4abcb-abb0-466a-bc58-274fa18b79af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 550bfac9b341d14b495c73e4426e8143d91d8e19
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947783"
---
# <a name="ui_pkey_keytip"></a><span data-ttu-id="0e531-103">UI- \_ pkey- \_ KeyTip</span><span class="sxs-lookup"><span data-stu-id="0e531-103">UI\_PKEY\_Keytip</span></span>

<span data-ttu-id="0e531-104">Bezeichnet die Benutzeroberflächen- \_ pkey- \_ KeyTip-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="0e531-104">Identifies the UI\_PKEY\_Keytip property.</span></span>

```
propertyDescription
   name = UI_PKEY_Keytip
   shellPKey = UI_PKEY_Keytip
   formatID = 00000003-7363-696e-8441798acf5aebb7
   propID = 3
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a><span data-ttu-id="0e531-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0e531-105">Remarks</span></span>

<span data-ttu-id="0e531-106">Der Benutzeroberflächen- \_ pkey- \_ KeyTip wird von einer Anwendung verwendet, um den Tastaturbeschleuniger eines Menüband-Steuer Elements abzufragen.</span><span class="sxs-lookup"><span data-stu-id="0e531-106">UI\_PKEY\_Keytip is used by an application to query the keyboard accelerator of a ribbon control.</span></span>

<span data-ttu-id="0e531-107">Dieser Eigenschafts Wert ist eine Zeichenfolge, die aus einer beliebigen Sequenz von Zeichen einschließlich Leerzeichen besteht.</span><span class="sxs-lookup"><span data-stu-id="0e531-107">This property value is a string, composed of any sequence of characters including white space.</span></span>

<span data-ttu-id="0e531-108">Der Wert von UI \_ pkey \_ KeyTip fungiert als Tastaturbeschleuniger für einen Befehl, es sei denn, dieser Befehl wird über ein Menü Element verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="0e531-108">The value of UI\_PKEY\_Keytip acts as the keyboard accelerator for a Command unless that Command is exposed through a menu item.</span></span> <span data-ttu-id="0e531-109">In diesem Fall ignoriert das Framework den Benutzeroberflächen- \_ pkey \_ -KeyTip-Wert und verwendet stattdessen ein Zeichen, dem ein kaufmännisches und-Zeichen vorangestellt ist, wie durch [**Command. labeltitle**](windowsribbon-element-command-labeltitle.md) oder [UI \_ pkey- \_ Bezeichnung](windowsribbon-reference-properties-uipkey-label.md)angegeben.</span><span class="sxs-lookup"><span data-stu-id="0e531-109">In this case, the framework ignores the UI\_PKEY\_Keytip value and instead uses a character preceded by an ampersand as specified by [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) or [UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md).</span></span> <span data-ttu-id="0e531-110">Wenn kein kaufmännisches und von der Bezeichnung " **Command. labeltitle** " oder "UI pkey" angegeben wird \_ \_ , wird kein KeyTip oder keine Tastatur Beschleunigung bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="0e531-110">If no ampersand is specified by **Command.LabelTitle** or UI\_PKEY\_Label, no keytip or keyboard accelerator is exposed.</span></span>

<span data-ttu-id="0e531-111">Die maximale Länge des UI- \_ pkey- \_ KeyTip ist unbegrenzt.</span><span class="sxs-lookup"><span data-stu-id="0e531-111">The maximum length of UI\_PKEY\_Keytip is unbounded.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0e531-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0e531-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e531-113">Ressourcen Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0e531-113">Resource Properties</span></span>](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[<span data-ttu-id="0e531-114">**Command. KeyTip**</span><span class="sxs-lookup"><span data-stu-id="0e531-114">**Command.Keytip**</span></span>](windowsribbon-element-command-keytip.md)
</dt> </dl>

 

 




