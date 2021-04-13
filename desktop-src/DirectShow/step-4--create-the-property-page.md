---
description: Schritt 4.
ms.assetid: ed71f26b-0812-4be8-96a4-b9f5dde45540
title: Schritt 4. Erstellen der Eigenschaften Seite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52e8ea1a22e30c57c66b263a62afc1e0cf801903
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218863"
---
# <a name="step-4-create-the-property-page"></a>Schritt 4. Erstellen der Eigenschaften Seite

An diesem Punkt unterstützt der Filter alle Elemente, die für eine Eigenschaften Seite benötigt werden. Der nächste Schritt besteht darin, die Eigenschaften Seite zu implementieren. Beginnen Sie, indem Sie eine neue Klasse von **cbasepropertypage** ableiten. Das folgende Beispiel zeigt einen Teil der Deklaration, einschließlich einiger private Member-Variablen, die später im Beispiel verwendet werden:


```C++
class CGrayProp : public CBasePropertyPage
{
private:
    ISaturation *m_pGray;    // Pointer to the filter's custom interface.
    long        m_lVal       // Store the old value, so we can revert.
    long        m_lNewVal;   // New value.
public:
    /* ... */
};
```



Erstellen Sie als nächstes eine Dialogfeld Ressource zusammen mit einer Zeichen folgen Ressource für den Dialog Titel im Ressourcen-Editor. Die Zeichenfolge wird auf der Registerkarte für die Eigenschaften Seite angezeigt. Die beiden Ressourcen-IDs sind Argumente für den **cbasepropertypage** -Konstruktor:


```C++
CGrayProp::CGrayProp(IUnknown *pUnk) : 
  CBasePropertyPage(NAME("GrayProp"), pUnk, IDD_PROPPAGE, IDS_PROPPAGE_TITLE),
  m_pGray(0)
{ }
```



Die folgende Abbildung zeigt die Dialog Ressource für die Beispiel Eigenschaften Seite.

![Eigenschaften Seiten Dialogfeld](images/proppage.png)

Nun sind Sie bereit, die Eigenschaften Seite zu implementieren. Die folgenden Methoden werden in **cbasepropertypage** zum Überschreiben angezeigt:

-   " **OnConnect** " wird aufgerufen, wenn der Client die Eigenschaften Seite erstellt. Der **IUnknown** -Zeiger wird auf den Filter festgelegt.
-   **Onaktivierungs** wird aufgerufen, wenn das Dialogfeld erstellt wird.
-   " **Onreceivemess Age** " wird aufgerufen, wenn das Dialogfeld eine Fenster Meldung empfängt.
-   " **Onapplychanges** " wird aufgerufen, wenn der Benutzer einen Commit für die Eigenschafts Änderungen durchführt, indem er auf **die Schaltfläche** **OK**
-   " **OnDisconnect** " wird aufgerufen, wenn der Benutzer das Eigenschaften Blatt schließt.

Im restlichen Teil dieses Tutorials wird jede dieser Methoden beschrieben.

Weiter: [Schritt 5. Speichert einen Zeiger auf den Filter](step-5--store-a-pointer-to-the-filter.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen einer Filter Eigenschaften Seite](creating-a-filter-property-page.md)
</dt> </dl>

 

 



