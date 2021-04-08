---
title: Insertable (CLSID-Schlüssel)
description: Gibt an, dass Objekte dieser Klasse im Listenfeld Objekt einfügen angezeigt werden sollen, wenn Sie von com-Container Anwendungen verwendet werden.
ms.assetid: 908cbfc4-ebf8-454e-b2e5-34449de60e7f
keywords:
- Insertable-Registrierungsschlüssel com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5da4892fb13de5954dabe7c55759900dba32f854
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104039994"
---
# <a name="insertable-clsid-key"></a><span data-ttu-id="d3d05-104">Insertable (CLSID-Schlüssel)</span><span class="sxs-lookup"><span data-stu-id="d3d05-104">Insertable (CLSID Key)</span></span>

<span data-ttu-id="d3d05-105">Gibt an, dass Objekte dieser Klasse im Listenfeld **Objekt einfügen** angezeigt werden sollen, wenn Sie von com-Container Anwendungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d3d05-105">Indicates that objects of this class should appear in the **Insert Object** dialog box list box when used by COM container applications.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="d3d05-106">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="d3d05-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Insertable
```

## <a name="remarks"></a><span data-ttu-id="d3d05-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d3d05-107">Remarks</span></span>

<span data-ttu-id="d3d05-108">Dieser Schlüssel ist ein erforderlicher Eintrag für 32-Bit-COM-Anwendungen, deren Objekte in vorhandene 16-Bit-Anwendungen eingefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="d3d05-108">This key is a required entry for 32-bit COM applications whose objects can be inserted into existing 16-bit applications.</span></span> <span data-ttu-id="d3d05-109">Vorhandene 16-Bit-Anwendungen suchen in der Registrierung nach diesem Schlüssel, der der Anwendung mitteilt, dass der Server Einbettungen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d3d05-109">Existing 16-bit applications look in the registry for this key, which informs the application that the server supports embeddings.</span></span> <span data-ttu-id="d3d05-110">Wenn der **Insertable** -Schlüssel vorhanden ist, versuchen 16-Bit-Anwendungen möglicherweise auch, zu überprüfen, ob der Server auf dem Computer vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="d3d05-110">If the **Insertable** key exists, 16-bit applications may also attempt to verify that the server exists on the machine.</span></span> <span data-ttu-id="d3d05-111">16-Bit-Anwendungen rufen in der Regel den Wert des [**LocalServer**](localserver.md) -Schlüssels aus der-Klasse ab und überprüfen, ob es sich um eine gültige Datei im System handelt.</span><span class="sxs-lookup"><span data-stu-id="d3d05-111">16-bit applications typically retrieve the value of the [**LocalServer**](localserver.md) key from the class and check to see whether it is a valid file on the system.</span></span> <span data-ttu-id="d3d05-112">Damit eine 32-Bit-Anwendung von einer 16-Bit-Anwendung einfügefähig ist, sollte die 32-Bit-Anwendung den **LocalServer** -Unterschlüssel zusätzlich zum Registrieren von [**LocalServer32**](localserver32.md)registrieren.</span><span class="sxs-lookup"><span data-stu-id="d3d05-112">Therefore, for a 32-bit application to be insertable by a 16-bit application, the 32-bit application should register the **LocalServer** subkey in addition to registering [**LocalServer32**](localserver32.md).</span></span>

<span data-ttu-id="d3d05-113">Dieser Eintrag wird mit-Steuerelementen verwendet und gibt an, dass ein Objekt nur als direktes eingebettetes Objekt ohne spezielle Steuerelement Funktionen fungieren kann.</span><span class="sxs-lookup"><span data-stu-id="d3d05-113">Used with controls, this entry indicates that an object can act only as an in-place embedded object with no special control features.</span></span> <span data-ttu-id="d3d05-114">Objekte mit diesem Schlüssel werden im Dialogfeld **Objekt einfügen** für ihren Container angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d3d05-114">Objects that have this key appear in the **Insert Object** dialog box for their container.</span></span> <span data-ttu-id="d3d05-115">Bei Verwendung mit-Steuerelementen gibt dieser Eintrag auch an, dass das Steuerelement mit nicht-Steuerelement Containern getestet wurde.</span><span class="sxs-lookup"><span data-stu-id="d3d05-115">When used with controls, this entry also indicates the control has been tested with non-control containers.</span></span> <span data-ttu-id="d3d05-116">Dieser Eintrag ist auch optional und kann ausgelassen werden, wenn ein Steuerelement nicht für die Arbeit mit älteren Containern konzipiert ist, die Steuerelemente nicht verstehen.</span><span class="sxs-lookup"><span data-stu-id="d3d05-116">This entry is also optional and can be omitted when a control is not designed to work with older containers that do not understand controls.</span></span>

> [!Note]  
> <span data-ttu-id="d3d05-117">Dieser Schlüssel ist nicht für interne Klassen wie die Monikerklassen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d3d05-117">This key is not present for internal classes like the moniker classes.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="d3d05-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d3d05-118">Related topics</span></span>

<dl> <dt>

[**<ProgID>**](-progid--key.md)
</dt> </dl>

 

 




