---
title: Verfügbar machen von Owner-Drawn Menü Elementen
description: Verfügbar machen von Owner-Drawn Menü Elementen
ms.assetid: 93b51cbb-b7b4-4a38-ba69-d6345a269944
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e79668115cedd5fb6b8c20b0d4df361d6d1d800
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515920"
---
# <a name="exposing-owner-drawn-menu-items"></a>Verfügbar machen von Owner-Drawn Menü Elementen

Anwendungsentwickler können die [**msaamenuinfo**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) -Struktur verwenden, um die Namen der Menü Elemente, die vom Besitzer gezeichnet werden, verfügbar zu machen. Durch Zuordnen dieser Struktur zu den Menü Elementdaten, die vom Besitzer gezeichnet werden, ist es nicht erforderlich, die Menü Elemente mit [**IAccessible verfügbar**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)zu machen.

Wenn Sie ein vom Besitzer gezeichnetes Menü erstellen, definieren Sie eine Klasse oder Struktur für die vom Besitzer gezeichneten Menü Elementdaten, und erstellen Sie für jedes Menü Element Instanzen dieser Klasse. Übergeben Sie einen Zeiger auf die Elementdaten, wenn Sie dem Menü Elemente hinzufügen.

Um die Namen der Menü Elemente verfügbar zu machen, muss die [**msaamenuinfo**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) -Struktur der erste Member der Struktur sein, die die anwendungsspezifischen Elementdaten definiert, wie im folgenden Beispiel gezeigt:


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



Die [**msaamenuinfo**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) -Struktur darf kein Member in einer Klasse sein, die virtuelle Funktionen enthält. Wenn der Code kompiliert wird, ist der erste Member der-Klasse immer ein vom Compiler generierter Zeiger auf eine Tabelle der virtuellen Funktionen. Um dieses Problem zu umgehen, erstellen Sie eine Elementdaten Struktur, die **msaamenuinfo** als ersten Member enthält. Der zweite Member ist ein Zeiger auf eine Instanz der-Klasse, die die vom Besitzer gezeichneten Daten definiert. Dieses Verfahren wird im folgenden Beispiel veranschaulicht.


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



Wenn Sie dem Menü Elemente hinzufügen, übergeben Sie einen Zeiger auf eine Instanz der-Struktur, die [**msaamenuinfo**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) enthält, um die Namen der Menü Elemente verfügbar zu machen.

 

 




