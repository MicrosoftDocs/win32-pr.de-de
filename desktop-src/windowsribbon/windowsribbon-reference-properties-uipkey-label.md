---
title: UI_PKEY_Label
description: Bezeichnet die Eigenschaft "UI \_ pkey \_ Label".
ms.assetid: 4d704133-bba7-4c32-a552-d748b66455eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 245ce8d239e1a0893c907a047aa9a48996cbf606
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856416"
---
# <a name="ui_pkey_label"></a><span data-ttu-id="a12b8-103">UI- \_ pkey- \_ Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="a12b8-103">UI\_PKEY\_Label</span></span>

<span data-ttu-id="a12b8-104">Bezeichnet die Eigenschaft "UI \_ pkey \_ Label".</span><span class="sxs-lookup"><span data-stu-id="a12b8-104">Identifies the UI\_PKEY\_Label property.</span></span>

```
propertyDescription
   name = UI_PKEY_Label
   shellPKey = UI_PKEY_Label
   formatID = 00000004-7363-696e-8441798acf5aebb7
   propID = 4
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a><span data-ttu-id="a12b8-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a12b8-105">Remarks</span></span>

<span data-ttu-id="a12b8-106">Die Benutzeroberflächen- \_ pkey- \_ Bezeichnung wird von einer Anwendung verwendet, um den Bezeichnungs Text von Registerkarten, Gruppen, Schaltflächen, Galerie Elementen und anderen Menü Band Steuerelementen abzufragen.</span><span class="sxs-lookup"><span data-stu-id="a12b8-106">UI\_PKEY\_Label is used by an application to query the label text of tabs, groups, buttons, gallery items, and other Ribbon controls.</span></span>

> [!Note]  
> <span data-ttu-id="a12b8-107">Windows 8 und höher: das Bild der [Anwendungsmenü](windowsribbon-controls-applicationmenu.md) Schaltfläche wurde in Bezeichnung: **File** geändert.</span><span class="sxs-lookup"><span data-stu-id="a12b8-107">Windows 8 and newer: [Application Menu](windowsribbon-controls-applicationmenu.md) button image changed to label: **File**.</span></span> <span data-ttu-id="a12b8-108">Es wird empfohlen, die Datei nicht als Bezeichnung für eine ihrer eigenen Registerkarten zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="a12b8-108">We recommend that you do not use File as the label for any of your own tabs.</span></span>

 

<span data-ttu-id="a12b8-109">Der Eigenschafts Wert ist eine Zeichenfolge, die auf eine beliebige Sequenz von Zeichen beschränkt ist, einschließlich Leerzeichen und Zeilenumbruch Zeichen.</span><span class="sxs-lookup"><span data-stu-id="a12b8-109">The property value is a string constrained to any sequence of characters, including white space and line-break characters.</span></span>

> [!Note]  
> <span data-ttu-id="a12b8-110">Verwenden Sie den XML-Zeichen Verweis Universal Character Set (UCS) `&#xA;` , um einen Zeilenumbruch anzugeben.</span><span class="sxs-lookup"><span data-stu-id="a12b8-110">Use the Universal Character Set (UCS) XML character reference `&#xA;` to specify a line break.</span></span>

 

<span data-ttu-id="a12b8-111">Die Rechte Ausrichtung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a12b8-111">Right alignment is not supported.</span></span>

<span data-ttu-id="a12b8-112">Die maximale Länge der UI- \_ pkey- \_ Bezeichnung ist unbegrenzt.</span><span class="sxs-lookup"><span data-stu-id="a12b8-112">The maximum length of UI\_PKEY\_Label is unbounded.</span></span>

<span data-ttu-id="a12b8-113">Wenn ein Befehl über ein Menü Element verfügbar gemacht wird und der Wert von [**Command. labeltitle**](windowsribbon-element-command-labeltitle.md) oder UI \_ pkey \_ Label einen Buchstaben enthält, dem ein kaufmännisches und vorangestellt ist, wie im folgenden Beispiel gezeigt, wird dieser Buchstabe sowohl als KeyTip als auch als Tastaturbeschleuniger für diesen Befehl durch das Multifunktionsleisten-Framework behandelt.</span><span class="sxs-lookup"><span data-stu-id="a12b8-113">If a Command is exposed through a menu item and the value of [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) or UI\_PKEY\_Label contains a letter preceded by an ampersand, as shown in the following example, this letter is treated as both a keytip and a keyboard accelerator for that Command by the Ribbon framework.</span></span>


```XML
<Command Name="cmdNew"
         Symbol="ID_FILE_NEW"
         Comment="New"
         Id="25001"
         LabelTitle="&amp;New"/>
```



<span data-ttu-id="a12b8-114">Um ein kaufmännisches und-Zeichen in einer Bezeichnung anzuzeigen, versehen Sie die Bezeichnung für Sonderzeichen mit einem doppelten kaufmännisches und-Zeichen ( `&&` ), wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="a12b8-114">To display an ampersand in a label, escape the special character designation with a double ampersand (`&&`) as shown in the following example.</span></span>


```XML
<Command Name="cmdOpen"
         Symbol="ID_FILE_OPEN"
         Comment="Open"
         Id="25002"
         LabelTitle="&amp;&amp;Open"/>
```



## <a name="related-topics"></a><span data-ttu-id="a12b8-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a12b8-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a12b8-116">Ressourcen Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a12b8-116">Resource Properties</span></span>](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[<span data-ttu-id="a12b8-117">**Command. labeltitle**</span><span class="sxs-lookup"><span data-stu-id="a12b8-117">**Command.LabelTitle**</span></span>](windowsribbon-element-command-labeltitle.md)
</dt> <dt>

[<span data-ttu-id="a12b8-118">UI \_ pkey \_ labeldescription</span><span class="sxs-lookup"><span data-stu-id="a12b8-118">UI\_PKEY\_LabelDescription</span></span>](windowsribbon-reference-properties-uipkey-labeldescription.md)
</dt> </dl>

 

 




