---
title: Verwenden von Value Map-Anmerkungen
description: Beispielcode finden Sie unter Beispiel für Value Map Annotation.
ms.assetid: 29be74c7-a7c2-41f4-8b94-5771988b74ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3a3e8d003d863372e21a413fad56bc93b977ee3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390372"
---
# <a name="using-value-map-annotation"></a>Verwenden von Value Map-Anmerkungen

**So erstellen Sie eine Werte Zuordnung**

1.  **Erstellen Sie eine Mapping-Zeichenfolge.**

    Eine Mapping-Zeichenfolge ist eine Liste der numerischen Werte eines Steuer Elements, die einer lesbaren Zeichenfolge in Unicode entsprechen. Er beginnt mit "a:" gefolgt von einer Zahl, die den Typ des verwendeten Indexes angibt. Nur Bild Indizes werden unterstützt. Daher ist der Indextyp immer 0.

    Auf die Zeichenfolge folgt: Index: result-Paare. Der Index ist eine Zahl, die einen Bildindex für einen List-View oder eine Strukturansicht darstellt, oder den Wert für ein Schieberegler-Steuerelement.

    Der resultierende Wert ist eine Zahl, die abgerufen wird, wenn Sie die Role-oder State-Eigenschaft für eine Listenansicht oder ein Strukturansicht-Steuerelement zuordnen. Diese Zahlen werden im Dezimal-oder Hexadezimal Format mit dem Präfix "0x" ausgedrückt.

    Die Mapping-Zeichenfolge wird immer mit einem abschließenden Doppelpunkt (":") beendet.

    Im folgenden finden Sie ein Beispiel für eine Anmerkung-Zuordnung für die Zustands-und Rollen Eigenschaften eines Kontrollkästchens in einer Listenansicht oder einem Strukturansicht-Steuerelement. Die Ansicht enthält zwei Elemente, die Kontrollkästchen darstellen, und jede enthält Bilder, die dem aktivierten und deaktivierten Zustand entsprechen.

    ```C++
    LPCWSTR g_ListOrTreeStateMap = 
    L"A:0"     // Index type; always 0. !
    L":0:0x00" // Image 0 is normal !
    L":1:0x10" // Image 1 is checked - STATE_SYSTEM_CHECKED (0x10) !
    L":";

    LPCWSTR g_ListOrTreeRoleMap = 
    L"A:0"     // Index type; always 0. !
    L":0:0x2C" // Image 0 is a check box - ROLE_SYSTEM_CHECKBUTTON
    (0x2c) !
    L":1:0x2C" // image 1 is also a check box !
    L":";
    ```

    

    Gültige Rollen-und Zustands Werte finden Sie unter [Objekt Rollen](object-roles.md) und [Objekt Zustands Konstanten](object-state-constants.md).

    Der Indexwert kann negativ sein, wenn Sie Eigenschaften für ein Schieberegler-Steuerelement zuordnen.

    Wenn Sie einen Wert oder eine Beschreibungs Eigenschaft zuordnen, ist das Ergebnis eine Zeichenfolge. Zeichen folgen werden nicht in Anführungszeichen eingeschlossen, und die Doppelpunkte fungieren als Trennzeichen.

    Weitere Informationen finden Sie unter [Annotation](value-map-annotation.md)-Zuordnungs Format.

2.  **Erstellen Sie den Anmerkung-Manager, und rufen Sie einen Zeiger auf seine**[**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices)-**Schnittstelle ab.**

    Im folgenden finden Sie ein Beispiel für die Erstellung des Anmerkung-Managers.

    ```C++
    IAccPropServices * pAccPropSvc = NULL;
    HRESULT hr = CoCreateInstance(CLSID_AccPropServices, NULL,
    CLSCTX_SERVER, IID_IAccPropServices, (void**) & pAccPropSvc));
    
    ```

    

3.  **Fügen Sie die Mapping-Zeichenfolge an das Steuerelement an**

    Wenden Sie [**IAccPropServices:: "abwndpropstr**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr)" an, indem Sie das **HWND** des Steuer Elements und einen Zeiger auf die Mapping-Zeichenfolge übergeben.

    Der *idProp* -Parameter ist einer der folgenden:

    

    | Parameter                   | Verwendung                                                |
    |-----------------------------|---------------------------------------------------------|
    | msaapropid- \_ rolemap         | So legen Sie eine Rollen Zuordnung für Listenansicht-oder Strukturansicht-Steuerelemente fest  |
    | msaapropid \_ statemap        | Zum Festlegen einer Zustands Zuordnung für Listenansicht-oder Strukturansicht-Steuerelemente. |
    | PROPID- \_ ACC- \_ deskriptionmap | Um eine Beschreibungs Zuordnung für Listenansicht-oder Struktur Ansichten festzulegen.   |
    | msaapropid \_ ValueMap        | Um eine Werte Zuordnung für Schieberegler-Steuerelemente festzulegen.                  |

    

     

4.  **Bereinigen.**

    Vor dem Zerstören von Werten, die mit Anmerkungen versehen sind (z. b. bei der Behandlung von [WM- \_ Zerstörung](../winmsg/wm-destroy.md)), müssen Sie zuvor registrierte Eigenschaften löschen und den Anmerkung-Manager freigeben.

    Dazu müssen Sie [**IAccPropServices:: clearhwnd-**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-clearhwndprops) Eigenschaften entsprechend aufrufen und den Zeiger auf [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices)freigeben.

Beispielcode finden Sie unter [Beispiel für Value Map Annotation](value-map-annotation-sample.md).

 

 