---
description: Implementieren Sie eine Eigenschaftenseite als Teil der Erstellung einer Filtereigenschaftenseite für einen benutzerdefinierten DirectShow-Filter.
ms.assetid: ed71f26b-0812-4be8-96a4-b9f5dde45540
title: Schritt 4. Erstellen der Eigenschaftenseite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d32cd9eacc98af5f273897a3837390ab5cc75f7a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406853"
---
# <a name="step-4-create-the-property-page"></a>Schritt 4. Erstellen der Eigenschaftenseite

An diesem Punkt unterstützt der Filter alles, was er für eine Eigenschaftenseite benötigt. Im nächsten Schritt wird die Eigenschaftenseite selbst implementiert. Beginnen Sie, indem Sie eine neue Klasse von **CBasePropertyPage** ableiten. Das folgende Beispiel zeigt einen Teil der Deklaration, einschließlich einiger privater Membervariablen, die später im Beispiel verwendet werden:


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



Erstellen Sie als Nächstes eine Dialogressource im Ressourcen-Editor zusammen mit einer Zeichenfolgenressource für den Dialogtitel. Die Zeichenfolge wird auf der Registerkarte für die Eigenschaftenseite angezeigt. Die beiden Ressourcen-IDs sind Argumente für den **CBasePropertyPage-Konstruktor:**


```C++
CGrayProp::CGrayProp(IUnknown *pUnk) : 
  CBasePropertyPage(NAME("GrayProp"), pUnk, IDD_PROPPAGE, IDS_PROPPAGE_TITLE),
  m_pGray(0)
{ }
```



Die folgende Abbildung zeigt die Dialogressource für die Beispieleigenschaftenseite.

![Dialogfeld "Eigenschaftenseite"](images/proppage.png)

Nun können Sie die Eigenschaftenseite implementieren. Hier sind die Methoden in **CBasePropertyPage,** die überschrieben werden sollen:

-   **OnConnect** wird aufgerufen, wenn der Client die Eigenschaftenseite erstellt. Er legt den **IUnknown-Zeiger** auf den Filter fest.
-   **OnActivate** wird aufgerufen, wenn das Dialogfeld erstellt wird.
-   **OnReceiveMessage** wird aufgerufen, wenn das Dialogfeld eine Fenstermeldung empfängt.
-   **OnApplyChanges** wird aufgerufen, wenn der Benutzer die Eigenschaftenänderungen committet, indem er auf die Schaltfläche **OK** oder **Übernehmen** klickt.
-   **OnDisconnect** wird aufgerufen, wenn der Benutzer das Eigenschaftenblatt verwarf.

Im weiteren Verlauf dieses Tutorials werden die einzelnen Methoden beschrieben.

Weiter: [Schritt 5. Speichern Sie einen Zeiger auf den Filter](step-5--store-a-pointer-to-the-filter.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen einer Filtereigenschaftenseite](creating-a-filter-property-page.md)
</dt> </dl>

 

 



