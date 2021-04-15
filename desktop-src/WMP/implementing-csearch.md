---
title: Implementieren von csearch
description: Implementieren von csearch
ms.assetid: 3041807a-e7e0-4022-ab90-a8b846bafc0e
keywords:
- Windows Media Player-Plug-ins, csearch-Klasse
- Plug-ins, csearch-Klasse
- Benutzeroberflächen-Plug-ins, csearch-Klasse
- UI-Plug-ins, csearch-Klasse
- Csearch-Klasse
- Programmier Handbuch, Benutzerschnittstellen-Plug-ins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f36c6446ca0eb6b1cc9dfb5f45044493c2a8fd6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515614"
---
# <a name="implementing-csearch"></a>Implementieren von csearch

Die **iwmppluginui** -Schnittstelle verfügt über mehrere Methoden, die von Windows Media Player zu unterschiedlichen Zeiten während des Lebenszyklus einer Plug-in-Instanz aufgerufen werden. Der Assistent stellt grundlegende Implementierungen dieser Methoden sowie den Klassenkonstruktor und-Dekonstruktor sowie andere Klassen Methoden bereit. Die Datei search. h muss geändert werden, damit Windows Media Player mit der Benutzeroberfläche kommunizieren kann, die im nächsten Abschnitt beschrieben wird.

Damit die cpluginwindow-Klasse Zugriff auf die private Member-Variable m \_ spcore hat, muss innerhalb der csearch-Klassendefinition eine Friend-Klassen Deklaration erstellt werden, wie im folgenden Code Ausschnitt gezeigt:


```C++
class ATL_NO_VTABLE CSearch : 
    public CComObjectRootEx<CComSingleThreadModel>,
    public CComCoClass<CSearch, &CLSID_Search>,
    public IWMPPluginUI
{

friend class CPluginWindow;

// Rest of class definition...

}

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmier Handbuch für Benutzeroberflächen-Plug-ins**](user-interface-plug-ins-programming-guide.md)
</dt> </dl>

 

 




