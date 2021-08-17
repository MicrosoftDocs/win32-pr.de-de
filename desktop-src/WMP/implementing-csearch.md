---
title: Implementieren von CSearch
description: Implementieren von CSearch
ms.assetid: 3041807a-e7e0-4022-ab90-a8b846bafc0e
keywords:
- Windows Media Player-Plug-Ins, CSearch-Klasse
- Plug-Ins, CSearch-Klasse
- Benutzeroberflächen-Plug-Ins, CSearch-Klasse
- Benutzeroberflächen-Plug-Ins, CSearch-Klasse
- CSearch-Klasse
- Programmierhandbuch, Benutzeroberflächen-Plug-Ins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56f99f3e232d11075bde9905169099649a3b6e754454ac10af60b8a83493fcd4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117748155"
---
# <a name="implementing-csearch"></a>Implementieren von CSearch

Die **IWMPPluginUI-Schnittstelle** verfügt über mehrere Methoden, die von Windows Media Player zu unterschiedlichen Zeiten während des Lebenszyklus einer Plug-In-Instanz aufgerufen werden. Der Assistent stellt grundlegende Implementierungen dieser Methoden sowie den Klassenkonstruktor und -destruktor sowie andere Klassenmethoden zur Anwendung. Die Datei Search.h muss geändert werden, damit Windows Media Player mit der Benutzeroberfläche kommunizieren kann. Dies wird im nächsten Abschnitt beschrieben.

Damit die CPluginWindow-Klasse Zugriff auf die private Membervariable m spCore hat, muss innerhalb der CSearch-Klassendefinition eine Friend-Klassendeklaration vorgenommen werden, wie im folgenden \_ Codeausschnitt gezeigt:


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

[**Benutzeroberfläche Plug-Ins -Programmierhandbuch**](user-interface-plug-ins-programming-guide.md)
</dt> </dl>

 

 




