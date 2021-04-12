---
title: Erstellen eines Objekts in com
description: Um eine COM-Schnittstelle zu verwenden, erstellt das Programm zuerst eine Instanz eines Objekts, das diese Schnittstelle implementiert.
ms.assetid: 75f2115d-d49d-4e4e-8f99-67a231559ba6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96f96e4d9c2afbac028bfcefffcec6a070c78c8b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390227"
---
# <a name="creating-an-object-in-com"></a>Erstellen eines Objekts in com

Nachdem ein Thread die com-Bibliothek initialisiert hat, ist es sicher, dass der Thread com-Schnittstellen verwendet. Um eine COM-Schnittstelle zu verwenden, erstellt das Programm zuerst eine Instanz eines Objekts, das diese Schnittstelle implementiert.

Im Allgemeinen gibt es zwei Möglichkeiten, ein COM-Objekt zu erstellen:

-   Das Modul, das das Objekt implementiert, kann möglicherweise eine Funktion bereitstellen, die speziell zum Erstellen von Instanzen dieses Objekts entworfen wurde.
-   Alternativ bietet com eine generische Erstellungs Funktion mit dem Namen [**cokreatabstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).

Nehmen Sie z. b. das hypothetische `Shape` Objekt aus dem Thema [Was ist eine COM-Schnittstelle?](what-is-a-com-interface-.md). In diesem Beispiel implementiert das- `Shape` Objekt eine-Schnittstelle mit dem Namen `IDrawable` . Die Grafikbibliothek, die das `Shape` Objekt implementiert, könnte eine Funktion mit der folgenden Signatur exportieren.


```C++
// Not an actual Windows function. 

HRESULT CreateShape(IDrawable** ppShape);
```



Mit dieser Funktion können Sie wie folgt ein neues- `Shape` Objekt erstellen.


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



Der *ppshape* -Parameter ist vom Typ "Pointer-to-Pointer-to-" `IDrawable` . Wenn Sie dieses Muster noch nicht gesehen haben, kann die doppelte Dereferenzierung verwirrend sein.

Beachten Sie die Anforderungen der- `CreateShape` Funktion. Die Funktion muss einen `IDrawable` Zeiger an den Aufrufer zurücksenden. Der Rückgabewert der Funktion wird jedoch bereits für den Fehler-/Erfolgscode verwendet. Daher muss der-Zeiger durch ein Argument für die-Funktion zurückgegeben werden. Der Aufrufer übergibt eine Variable vom Typ `IDrawable*` an die Funktion, und die Funktion überschreibt diese Variable mit einem neuen `IDrawable` Zeiger. In C++ gibt es nur zwei Möglichkeiten, wie eine Funktion einen Parameterwert überschreiben kann: "Pass-by-Reference" oder "Pass by address". COM verwendet die letztgenannte Pass-by-address. Und die Adresse eines Zeigers ist ein Zeiger auf einen Zeiger, daher muss der Parametertyp sein `IDrawable**` .

Im folgenden finden Sie ein Diagramm, mit dem Sie visualisieren können, was passiert.

![Diagramm, das die doppelte Zeiger Dereferenzierung anzeigt](images/com03.png)

Die- `CreateShape` Funktion verwendet die Adresse von *pshape* ( `&pShape` ), um einen neuen Zeiger Wert in *pshape* zu schreiben.

## <a name="cocreateinstance-a-generic-way-to-create-objects"></a>Cokreatanstance: eine generische Methode zum Erstellen von Objekten

Die [**cokreateinzustance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion stellt einen generischen Mechanismus zum Erstellen von-Objekten bereit. Beachten Sie, dass zwei COM-Objekte die gleiche Schnittstelle implementieren können und ein Objekt zwei oder mehr Schnittstellen implementieren kann, um **cokreateinstance** nachzuvollziehen. Daher benötigt eine generische Funktion, die-Objekte erstellt, zwei Informationen.

-   Welches Objekt erstellt werden soll.
-   Die Schnittstelle, die vom-Objekt abgeleitet werden soll.

Aber wie geben wir diese Informationen an, wenn wir die Funktion bezeichnen? In com wird ein Objekt oder eine Schnittstelle durch Zuweisen einer 128-Bit-Nummer identifiziert, die als *Globally Unique Identifier* (GUID) bezeichnet wird. GUIDs werden auf eine Weise generiert, die Sie effektiv eindeutig macht. GUIDs stellen eine Lösung für das Problem dar, wie eindeutige Bezeichner ohne zentrale Registrierungsstelle erstellt werden. GUIDs werden manchmal als *universell eindeutige* Bezeichner (UUIDs) bezeichnet. Vor com wurden Sie in DCE/RPC verwendet (verteilte Computerumgebung/Remote Prozedur Aufruf). Zum Erstellen neuer GUIDs sind mehrere Algorithmen vorhanden. Nicht alle diese Algorithmen garantieren die Eindeutigkeit streng, aber die Wahrscheinlichkeit, dass der gleiche GUID-Wert zweimal erstellt wird, ist extrem klein – effektiv 0 (null). GUIDs können verwendet werden, um jede Art von Entität zu identifizieren, nicht nur Objekte und Schnittstellen. Dies ist jedoch die einzige Verwendung, die uns in diesem Modul betrifft.

Beispielsweise kann die `Shapes` Bibliothek zwei GUID-Konstanten deklarieren:


```C++
extern const GUID CLSID_Shape;
extern const GUID IID_IDrawable; 
```



(Sie können davon ausgehen, dass die tatsächlichen numerischen 128-Bit-Werte für diese Konstanten an anderer Stelle definiert sind.) Die Konstante **CLSID- \_ Form** identifiziert das `Shape` Objekt, während die Konstante **IID \_ idrawable** die `IDrawable` Schnittstelle identifiziert. Das Präfix "CLSID" steht für den *Klassen Bezeichner*, und die Präfix- *IID* steht für den *Schnittstellen Bezeichner*. Dabei handelt es sich um Standard Benennungs Konventionen in com.

Wenn Sie diese Werte haben, würden Sie `Shape` wie folgt eine neue Instanz erstellen:


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



Die [**cokreateinzustance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion hat fünf Parameter. Der erste und vierte Parameter sind der Klassen Bezeichner und der Schnittstellen Bezeichner. Tatsächlich teilen diese Parameter die Funktion "Create the Shape Object" und geben mir einen Zeiger auf die idrawable-Schnittstelle.

Legen Sie den zweiten Parameter auf **null** fest. (Weitere Informationen zur Bedeutung dieses Parameters finden Sie im Thema [Aggregation](/windows/desktop/com/aggregation) in der com-Dokumentation.) Der dritte Parameter nimmt einen Satz von Flags an, dessen Hauptzweck darin besteht, den *Ausführungs Kontext* für das Objekt anzugeben. Der Ausführungs Kontext gibt an, ob das Objekt in demselben Prozess wie die Anwendung ausgeführt wird. in einem anderen Prozess auf demselben Computer oder auf einem Remote Computer. In der folgenden Tabelle werden die gängigsten Werte für diesen Parameter angezeigt.



| Flag                       | Beschreibung                                                                                                                                                        |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CLSCTX- \_ INPROC- \_ Server** | Der gleiche Prozess.                                                                                                                                                      |
| **lokaler CLSCTX- \_ \_ Server**  | Anderer Prozess, gleicher Computer.                                                                                                                                  |
| **CLSCTX- \_ Remote \_ Server** | Anderer Computer.                                                                                                                                                |
| **Alle CLSCTX \_**            | Verwenden Sie die effizienteste Option, die vom-Objekt unterstützt wird. (Die Rangfolge, von der effizientesten bis zum geringsten Effizienz, ist: Prozess interne, Prozess-und Computer übergreifend.) |



 

Die Dokumentation für eine bestimmte Komponente kann Ihnen mitteilen, welchen Ausführungs Kontext das Objekt unterstützt. Wenn nicht, verwenden Sie " **CLSCTX \_ all**". Wenn Sie einen Ausführungs Kontext anfordern, der vom Objekt nicht unterstützt wird, gibt die [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion den Fehlercode **RegDB \_ E \_ classnotreg** zurück. Dieser Fehlercode kann auch darauf hindeuten, dass die CLSID keiner Komponente entspricht, die auf dem Computer des Benutzers registriert ist.

Der fünfte Parameter für [**cokreateingestance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) erhält einen Zeiger auf die-Schnittstelle. Da **cokreateingestance** ein generischer Mechanismus ist, kann dieser Parameter nicht stark typisiert sein. Stattdessen ist der Datentyp " **void \* \***", und der Aufrufer muss die Adresse des Zeigers in **einen \* \* void** -Typ umwandeln. Dies ist der Zweck der **erneuten interpretierungsumwandlung \_** im vorherigen Beispiel.

Es ist wichtig, dass Sie den Rückgabewert von [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)überprüfen. Wenn die Funktion einen Fehlercode zurückgibt, ist der COM-Schnittstellen Zeiger ungültig. der Versuch, ihn zu dereferenzieren, kann dazu führen, dass das Programm abstürzt.

Intern verwendet die [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion verschiedene Techniken, um ein Objekt zu erstellen. Im einfachsten Fall wird der Klassen Bezeichner in der Registrierung nachgeschlagen. Der Registrierungs Eintrag verweist auf eine DLL oder exe, die das Objekt implementiert. Von **cokreateinstance** können auch Informationen aus einem com+-Katalog oder einem parallelen (SxS) Manifest verwendet werden. Unabhängig davon sind die Details für den Aufrufer transparent. Weitere Informationen zu den internen Details von **cokreateinstance** finden Sie unter [com-Clients und-Server](/windows/desktop/com/com-clients-and-servers).

Das `Shapes` Beispiel, das wir bereits verwendet haben, ist etwas verwirrend. Nun können wir nun ein Beispiel für com in Aktion aktivieren: Anzeigen des Dialog Felds **Öffnen** , in dem der Benutzer eine Datei auswählen kann.

## <a name="next"></a>Nächste

[Beispiel: das Dialog Feld "Öffnen"](example--the-open-dialog-box.md)

 

 