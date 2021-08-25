---
title: Erstellen eines Objekts in COM
description: Um eine COM-Schnittstelle zu verwenden, erstellt Ihr Programm zuerst eine Instanz eines Objekts, das diese Schnittstelle implementiert.
ms.assetid: 75f2115d-d49d-4e4e-8f99-67a231559ba6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7e15874e1d4dcb6bc29fad90f40f90b478c805ccc7b0d0085f560a8b56e2247
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913765"
---
# <a name="creating-an-object-in-com"></a>Erstellen eines Objekts in COM

Nachdem ein Thread die COM-Bibliothek initialisiert hat, ist es sicher, dass der Thread COM-Schnittstellen verwendet. Um eine COM-Schnittstelle zu verwenden, erstellt Ihr Programm zuerst eine Instanz eines Objekts, das diese Schnittstelle implementiert.

Im Allgemeinen gibt es zwei Möglichkeiten, ein COM-Objekt zu erstellen:

-   Das Modul, das das -Objekt implementiert, stellt möglicherweise eine Funktion zur Verfügung, die speziell zum Erstellen von Instanzen dieses Objekts entwickelt wurde.
-   Alternativ stellt COM eine generische Erstellungsfunktion namens [**CoCreateInstance zur Verfügung.**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)

Nehmen Sie beispielsweise das hypothetische Objekt aus `Shape` dem Thema Was ist eine [COM-Schnittstelle?](what-is-a-com-interface-.md). In diesem Beispiel implementiert das `Shape` -Objekt eine Schnittstelle namens `IDrawable` . Die Grafikbibliothek, die das `Shape` -Objekt implementiert, kann eine Funktion mit der folgenden Signatur exportieren.


```C++
// Not an actual Windows function. 

HRESULT CreateShape(IDrawable** ppShape);
```



Mit dieser Funktion können Sie wie folgt ein `Shape` neues -Objekt erstellen.


```C++
IDrawable *pShape;

HRESULT hr = CreateShape(&pShape);
if (SUCCEEDED(hr))
{
    // Use the Shape object.
}
else
{
    // An error occurred.
}
```



Der *ppShape-Parameter* ist vom Typ pointer-to-pointer-to- `IDrawable` . Wenn Sie dieses Muster noch nicht gesehen haben, kann die doppelte Deskription verziffen sein.

Berücksichtigen Sie die Anforderungen der `CreateShape` Funktion. Die Funktion muss einen `IDrawable` Zeiger zurück zum Aufrufer geben. Der Rückgabewert der Funktion wird jedoch bereits für den Fehler-/Erfolgscode verwendet. Daher muss der Zeiger über ein Argument an die Funktion zurückgegeben werden. Der Aufrufer überschreibt eine Variable vom Typ an die Funktion, und die Funktion überschreibt diese Variable mit `IDrawable*` einem `IDrawable` neuen Zeiger. In C++ gibt es nur zwei Möglichkeiten für eine Funktion, einen Parameterwert zu überschreiben: Als Verweis übergeben oder als Adresse übergeben. COM verwendet letztere Pass-by-Adresse. Und die Adresse eines Zeigers ist ein Zeiger auf einen Zeiger, daher muss der Parametertyp `IDrawable**` sein.

Hier sehen Sie ein Diagramm, das Sie beim Visualisieren der vor sich gehenden Daten hilft.

![Diagramm mit doppelter Zeigerdeskription](images/com03.png)

Die `CreateShape` Funktion verwendet die Adresse von *pShape* ( ), um einen neuen `&pShape` Zeigerwert auf *pShape zu schreiben.*

## <a name="cocreateinstance-a-generic-way-to-create-objects"></a>CoCreateInstance: Eine generische Möglichkeit zum Erstellen von Objekten

Die [**CoCreateInstance-Funktion**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) bietet einen generischen Mechanismus zum Erstellen von Objekten. Um **CoCreateInstance zu** verstehen, beachten Sie, dass zwei COM-Objekte dieselbe Schnittstelle implementieren können und ein Objekt zwei oder mehr Schnittstellen implementieren kann. Daher benötigt eine generische Funktion, die Objekte erstellt, zwei Informationen.

-   Das zu erstellende Objekt.
-   Welche Schnittstelle aus dem -Objekt erhalten werden soll.

Aber wie geben wir diese Informationen an, wenn wir die Funktion aufrufen? In COM wird ein Objekt oder eine Schnittstelle identifiziert, indem ihm eine 128-Bit-Zahl zugewiesen wird, die als *globally unique identifier* (GUID) bezeichnet wird. GUIDs werden auf eine Weise generiert, die sie effektiv eindeutig macht. GUIDs sind eine Lösung für das Problem, eindeutige Bezeichner ohne zentrale Registrierungsstelle zu erstellen. GUIDs werden manchmal als *UUIDs (Universally Unique Identifier)* bezeichnet. Vor COM wurden sie in DCE/RPC (Distributed Computing Environment/Remote Procedure Call) verwendet. Es gibt mehrere Algorithmen zum Erstellen neuer GUIDs. Nicht alle diese Algorithmen garantieren genau die Eindeutigkeit, aber die Wahrscheinlichkeit, dass derselbe GUID-Wert versehentlich zweimal erstellt wird, ist äußerst klein – effektiv 0 (null). GUIDs können verwendet werden, um eine beliebige Art von Entität zu identifizieren, nicht nur Objekte und Schnittstellen. Dies ist jedoch die einzige Verwendung, die uns in diesem Modul betrifft.

Beispielsweise kann die `Shapes` Bibliothek zwei GUID-Konstanten deklarieren:


```C++
extern const GUID CLSID_Shape;
extern const GUID IID_IDrawable; 
```



(Sie können davon ausgehen, dass die tatsächlichen numerischen 128-Bit-Werte für diese Konstanten an anderer Stelle definiert sind.) Die konstante **CLSID-Form \_** identifiziert das Objekt, während die `Shape` Konstante **IID \_ IDrawable** die Schnittstelle `IDrawable` identifiziert. Das Präfix "CLSID" steht für *Klassenbezeichner,* und das *Präfix IID steht* für *Schnittstellenbezeichner*. Dies sind Standardbenennungskonventionen in COM.

Bei diesen Werten würden Sie wie folgt eine `Shape` neue -Instanz erstellen:


```C++
IDrawable *pShape;
hr = CoCreateInstance(CLSID_Shape, NULL, CLSCTX_INPROC_SERVER, IID_Drawable,
     reinterpret_cast<void**>(&pShape));

if (SUCCEEDED(hr))
{
    // Use the Shape object.
}
else
{
    // An error occurred.
}
```



Die [**CoCreateInstance-Funktion**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) verfügt über fünf Parameter. Der erste und vierte Parameter sind der Klassenbezeichner und der Schnittstellenbezeichner. Tatsächlich weisen diese Parameter die Funktion an: "Create the Shape object, and give me a pointer to the IDrawable interface." (Erstellen Sie das Shape-Objekt, und weisen Sie mir einen Zeiger auf die IDrawable-Schnittstelle zu.)

Legen Sie den zweiten Parameter auf **NULL fest.** (Weitere Informationen zur Bedeutung dieses Parameters finden Sie im Thema [Aggregation](/windows/desktop/com/aggregation) in der COM-Dokumentation.) Der dritte Parameter akzeptiert eine Reihe von Flags, deren Hauptzweck die Angabe *des* Ausführungskontexts für das Objekt ist. Der Ausführungskontext gibt an, ob das Objekt im gleichen Prozess wie die Anwendung ausgeführt wird. in einem anderen Prozess auf demselben Computer; oder auf einem Remotecomputer. In der folgenden Tabelle sind die gängigsten Werte für diesen Parameter aufgeführt.



| Flag                       | Beschreibung                                                                                                                                                        |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CLSCTX \_ INPROC \_ SERVER** | Der gleiche Prozess.                                                                                                                                                      |
| **LOKALER \_ CLSCTX-SERVER \_**  | Unterschiedlicher Prozess, gleicher Computer.                                                                                                                                  |
| **CLSCTX-REMOTESERVER \_ \_** | Unterschiedlicher Computer.                                                                                                                                                |
| **CLSCTX \_ ALL**            | Verwenden Sie die effizienteste Option, die das -Objekt unterstützt. (Die Rangfolge , von der effizientesten zur am wenigsten effizienten, ist: in-process, out-of-process und cross-computer.) |



 

Die Dokumentation für eine bestimmte Komponente kann Ihnen mitteilen, welcher Ausführungskontext das Objekt unterstützt. Wenn nicht, verwenden Sie **CLSCTX \_ ALL**. Wenn Sie einen Ausführungskontext anfordern, der vom -Objekt nicht unterstützt wird, gibt die [**CoCreateInstance-Funktion**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) den Fehlercode **REGDB \_ E \_ CLASSNOTREG zurück.** Dieser Fehlercode kann auch darauf hinweisen, dass die CLSID nicht einer Komponente entspricht, die auf dem Computer des Benutzers registriert ist.

Der fünfte Parameter für [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) empfängt einen Zeiger auf die -Schnittstelle. Da **CoCreateInstance ein** generischer Mechanismus ist, kann dieser Parameter nicht stark typisiert werden. Stattdessen ist der Datentyp **void, \* \*** und der Aufrufer muss die Adresse des Zeigers auf einen void-Typ **\* \* umerkennen.** Dies ist der Zweck der **Neuinterpret-Cast \_ im** vorherigen Beispiel.

Es ist wichtig, den Rückgabewert von [**CoCreateInstance zu überprüfen.**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) Wenn die Funktion einen Fehlercode zurückgibt, ist der COM-Schnittstellenzeiger ungültig, und der Versuch, ihn zu dereferenzieren, kann zu einem Absturz des Programms führen.

Intern verwendet die [**CoCreateInstance-Funktion**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) verschiedene Techniken, um ein Objekt zu erstellen. Im einfachsten Fall sucht es den Klassenbezeichner in der Registrierung. Der Registrierungseintrag verweist auf eine DLL oder EXE, die das -Objekt implementiert. **CoCreateInstance kann** auch Informationen aus einem COM+-Katalog oder einem SxS-Manifest (Side-by-Side) verwenden. Unabhängig davon sind die Details für den Aufrufer transparent. Weitere Informationen zu den internen Details von **CoCreateInstance finden** Sie unter [COM-Clients und -Server.](/windows/desktop/com/com-clients-and-servers)

Das Beispiel, das wir verwendet haben, ist etwas unerschädig. Sehen wir uns nun ein reales Beispiel für COM in Aktion an: Anzeigen des Dialogfelds Öffnen, in dem der Benutzer eine Datei auswählen `Shapes` kann. 

## <a name="next"></a>Nächste

[Beispiel: Das Dialogfeld "Öffnen"](example--the-open-dialog-box.md)

 

 