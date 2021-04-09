---
title: Schnittstellen Entwurfs Regeln
description: Dieser Abschnitt enthält eine kurze Zusammenfassung der Schnittstellen Entwurfs Regeln und-Richtlinien.
ms.assetid: c43fc385-bcd6-45fc-91b2-ad9827fdb15c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c1cde73527ac79a2e4442910e3053ed96748337
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104102383"
---
# <a name="interface-design-rules"></a>Schnittstellen Entwurfs Regeln

Dieser Abschnitt enthält eine kurze Zusammenfassung der Schnittstellen Entwurfs Regeln und-Richtlinien. Einige dieser Regeln gelten speziell für die com-Architektur, während andere Einschränkungen von der Programmiersprache "Interface", "Mittel l", verursacht werden. Details zum Design der COM-Schnittstelle finden Sie unter [Anatomie einer IDL-Datei](anatomy-of-an-idl-file.md).

Definitionsgemäß ist ein Objekt kein COM-Objekt, es sei denn, es implementiert entweder die [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) -Schnittstelle oder eine Schnittstelle, die von **IUnknown** abgeleitet ist. Außerdem gelten die folgenden Regeln für alle für ein COM-Objekt implementierten Schnittstellen:

-   Sie müssen über einen eindeutigen Schnittstellen Bezeichner (IID) verfügen.
-   Sie müssen unveränderlich sein. Nachdem Sie erstellt und veröffentlicht wurden, kann sich kein Teil ihrer Definition ändern.
-   Alle Schnittstellen Methoden müssen einen **HRESULT** -Wert zurückgeben, damit die Teile des Systems, die die Remote Verarbeitung verarbeiten, RPC-Fehler melden können.
-   Alle Zeichen folgen Parameter in Schnittstellen Methoden müssen Unicode sein.
-   Die Datentypen müssen Remote fähig sein. Wenn Sie einen-Datentyp nicht in einen Remote fähigen Typ konvertieren können, müssen Sie eigene Marshalling-und Marshallingroutinen erstellen. Außerdem hat **LPVOID** oder **void \*** keine Bedeutung auf einem Remote Computer. Verwenden Sie ggf. einen Zeiger auf [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown).

> [!Note]  
> Die aktuelle Implementierung von "Mittel l" verarbeitet keine Funktions Überladung oder mehrfache Vererbung.

 

## <a name="other-interface-design-considerations"></a>Weitere Überlegungen zur Schnittstellen Entwicklung

Verwenden Sie Verweise auf Daten sehr sorgfältig. Um die Daten im Adressraum des aufgerufenen Prozesses neu zu erstellen, muss die RPC-Laufzeit die genaue Größe der Daten kennen. Wenn z. b. ein **Char \*** -Parameter auf einen Puffer von Zeichen anstelle eines einzelnen Zeichens zeigt, können die Daten nicht ordnungsgemäß neu erstellt werden. Verwenden Sie die Syntax, die in der mittleren l verfügbar ist, um die durch ihre Typdefinitionen dargestellten Datenstrukturen genau zu beschreiben.

Die Initialisierung ist für Zeiger von Bedeutung, die in Arrays und Strukturen eingebettet sind und über Prozess Grenzen hinweg übertragen werden. Nicht initialisierte Zeiger funktionieren möglicherweise, wenn Sie an ein Programm im selben Prozessbereich übermittelt werden, Proxys und stubvorgänge gehen jedoch davon aus, dass alle Zeiger mit gültigen Adressen initialisiert werden oder NULL sind.

Gehen Sie beim Aliasing von Zeigern vorsichtig vor (sodass Zeiger auf denselben Arbeitsspeicher zeigen). Wenn das Aliasing beabsichtigt ist, sollten diese Zeiger in der IDL-Datei als Alias deklariert werden. Zeiger, die als nicht-Alias deklariert sind, sollten niemals einander als Alias aufweisen.

Achten Sie darauf, wie Sie Arbeitsspeicher zuordnen und freigeben. Wenn Sie ein COM-Objekt (mithilfe des Attributs " [**zuordnen**](/windows/desktop/Midl/allocate) ") nicht explizit angeben, um eine Datenstruktur, die während eines Out-of-Process-Aufrufes erstellt wurde, nicht freizugeben, wird diese Struktur beim Abschluss des Aufrufes zerstört. Beachten Sie auch den potenziell destruktiven Aufwand, der durch eine ineffiziente Zuordnung von Datenstrukturen entsteht, die jetzt gemarshallt und gemarshallt werden müssen.

Beachten Sie abschließend beim Definieren der **HRESULT** -Rückgabewerte, dass Sie keine Fehlercodes erstellen, die mit com-definierten Einrichtung-Codes in Konflikt \_ stehen (Werte zwischen 0x0000 und 0x01ff sind reserviert) oder die mit anderen **HRESULT** -Werten mit demselben Wert in Konflikt stehen. Verwenden Sie nach Möglichkeit die Rückgabewerte für den universellen com-Erfolg und den Fehler, und verwenden [**Sie einen Out**](/windows/desktop/Midl/out-idl) -Parameter anstelle eines **HRESULT**, um spezifische Informationen für den Funktionsaufruf zurückzugeben.

Weitere Informationen finden Sie unter den folgenden Themen:

-   [Entwerfen von Remote fähigen Schnittstellen](designing-remotable-interfaces.md)
-   [Verwenden einer COM-Schnittstelle](using-a-com-interface.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schnittstellendefinitionen und Typbibliotheken](/windows/desktop/Midl/interface-definitions-and-type-libraries)
</dt> </dl>

 

 