---
title: Verfügbar machen Owner-Drawn Menüelemente
description: Verfügbar machen Owner-Drawn Menüelemente
ms.assetid: 93b51cbb-b7b4-4a38-ba69-d6345a269944
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c84a2630b5227937d4a1c9621360d9fb028676bba03516970f93e314b382035b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860500"
---
# <a name="exposing-owner-drawn-menu-items"></a>Verfügbar machen Owner-Drawn Menüelemente

Anwendungsentwickler können die [**MSAAMENUINFO-Struktur**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) verwenden, um die Namen von Vom Besitzer gezeichneten Menüelementen verfügbar zu machen. Indem Sie diese Struktur den Daten des vom Besitzer gezeichneten Menüelements zuordnen, müssen Sie die Menüelemente nicht mit [**IAccessible verfügbar machen.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

Definieren Sie beim Erstellen eines besitzergezeichneten Menüs eine Klasse oder Struktur für die Daten des vom Besitzer gezeichneten Menüelements, und erstellen Sie Instanzen dieser Klasse für jedes Menüelement. Übergeben Sie beim Hinzufügen von Elementen zum Menü einen Zeiger auf die Elementdaten.

Um die Namen der Menüelemente verfügbar zu machen, muss die [**MSAAMENUINFO-Struktur**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) das erste Element der Struktur sein, die die anwendungsspezifischen Elementdaten definiert, wie im folgenden Beispiel gezeigt:


```C++
// Application-specific owner-drawn menu info struct. Owner-drawn data 
// is a pointer to one of these.
struct MenuEntry
{
    MSAAMENUINFO m_MSAA;       // MSAA info - must be first member
    LPTSTR       m_pName;      // Displayed menu text or NULL for 
                               //   separator item 
    int          m_CmdID;      // Menu command ID 
    int          m_IconIndex;  // Index of icon in bitmap or -1 for
                               //   for separator 
};
```



Die [**MSAAMENUINFO-Struktur**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) darf kein Member in einer Klasse sein, die virtuelle Funktionen enthält. Wenn der Code kompiliert wird, ist der erste Member der -Klasse immer ein vom Compiler generierter Zeiger auf eine Tabelle der virtuellen Funktionen. Um dieses Problem zu beheben, erstellen Sie eine Elementdatenstruktur, die **MSAAMENUINFO** als erstes Element enthält. Der zweite Member ist ein Zeiger auf eine Instanz der -Klasse, die die vom Besitzer gezeichneten Daten definiert. Im folgenden Beispiel wird diese Technik veranschaulicht.


```C++
// Application-defined class that contains the owner-drawn data and 
//  virtual functions that operate on that data.  
class MenuEntry
{
    LPTSTR       m_pName;      // Displayed menu text or NULL for 
                               //  separator item. 
    int          m_CmdID;      // Menu command ID 
    int          m_IconIndex;  // Index of icon in bitmap or -1 for
                               //  separator item 
    virtual void m_AnimateIcon();  
    virtual void m_ChangeIconColor();
}

// Application-defined struct that contains MSAAMENUINFO as first 
//  member. Second member points to owner-drawn data. 
struct MenuInfo
{
    MSAAMENUINFO m_MSAA;       // MSAA info - must be first member
    MenuEntry *pMenuData;      // Points to the owner-drawn data 
}
```



Übergeben Sie beim Hinzufügen von Elementen zum Menü einen Zeiger auf eine Instanz der -Struktur, die [**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) enthält, um die Namen der Menüelemente verfügbar zu machen.

 

 




