---
title: Schnittstellenentwurfsregeln
description: Dieser Abschnitt enthält eine kurze Zusammenfassung der Regeln und Richtlinien für den Schnittstellenentwurf.
ms.assetid: c43fc385-bcd6-45fc-91b2-ad9827fdb15c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58d11d55a1e24c02208ebeecddd5a4f90b8b01fa4a53444e6554cfcff37165f4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070810"
---
# <a name="interface-design-rules"></a>Schnittstellenentwurfsregeln

Dieser Abschnitt enthält eine kurze Zusammenfassung der Regeln und Richtlinien für den Schnittstellenentwurf. Einige dieser Regeln sind spezifisch für die COM-Architektur, während andere Einschränkungen sind, die von der Schnittstellenentwurfssprache MIDL erzwungen werden. Ausführliche Informationen zum Entwurf der COM-Schnittstelle finden Sie unter [Aufbau einer IDL-Datei.](anatomy-of-an-idl-file.md)

Definitionsgemäß ist ein Objekt kein COM-Objekt, es sei denn, es implementiert entweder die [**IUnknown-Schnittstelle**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) oder eine Schnittstelle, die von **IUnknown** abgeleitet ist. Darüber hinaus gelten die folgenden Regeln für alle Schnittstellen, die in einem COM-Objekt implementiert sind:

-   Sie müssen über einen eindeutigen Schnittstellenbezeichner (Unique Interface Identifier, IID) verfügen.
-   Sie müssen unveränderlich sein. Nachdem sie erstellt und veröffentlicht wurden, kann sich kein Teil ihrer Definition ändern.
-   Alle Schnittstellenmethoden müssen einen **HRESULT-Wert** zurückgeben, damit die Teile des Systems, die die Remoteverarbeitung verarbeiten, RPC-Fehler melden können.
-   Alle Zeichenfolgenparameter in Schnittstellenmethoden müssen Unicode sein.
-   Ihre Datentypen müssen remotable sein. Wenn Sie einen Datentyp nicht in einen remotablen Typ konvertieren können, müssen Sie eigene Marshalling- und Unmarshalingroutinen erstellen. Außerdem hat **LPVOID** oder **\* void* _auf einem Remotecomputer keine Bedeutung. Verwenden Sie bei Bedarf einen Zeiger auf [_ *IUnknown.* *](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)

> [!Note]  
> Die aktuelle Implementierung von MIDL behandelt keine Funktionsüberladung oder mehrfache Vererbung.

 

## <a name="other-interface-design-considerations"></a>Weitere Überlegungen zum Schnittstellenentwurf

Verwenden Sie Zeiger auf Daten sehr sorgfältig. Um die Daten im Adressraum des aufgerufenen Prozesses neu zu erstellen, muss die RPC-Laufzeit die genaue Größe der Daten kennen. Wenn beispielsweise ein **\* CHAR-Parameter** auf einen Zeichenpuffer und nicht auf ein einzelnes Zeichen zeigt, können die Daten nicht ordnungsgemäß neu erstellt werden. Verwenden Sie die in MIDL verfügbare Syntax, um die datenstrukturen, die durch Ihre Typdefinitionen dargestellt werden, genau zu beschreiben.

Die Initialisierung ist wichtig für Zeiger, die in Arrays und Strukturen eingebettet und über Prozessgrenzen hinweg übergeben werden. Nicht initialisierte Zeiger können funktionieren, wenn sie an ein Programm im gleichen Prozessbereich übergeben werden, aber Proxys und Stubs gehen davon aus, dass alle Zeiger mit gültigen Adressen initialisiert werden oder NULL sind.

Seien Sie beim Aliasing von Zeigern vorsichtig (sodass Zeiger auf denselben Arbeitsspeicher zeigen können). Wenn das Aliasing beabsichtigt ist, sollten diese Zeiger in der IDL-Datei als Alias deklariert werden. Zeiger, die als nicht gealiased deklariert sind, dürfen nie einen Alias untereinander verwenden.

Achten Sie darauf, wie Sie Arbeitsspeicher zuordnen und freigeben. Denken Sie daran, dass diese Struktur nach Abschluss des Aufrufs zerstört wird, es sei denn, Sie weisen einem COM-Objekt (mithilfe des [**Attributs allocate)**](/windows/desktop/Midl/allocate) explizit an, keine Datenstruktur freizustellen, die während eines Out-of-Process-Aufrufs erstellt wurde. Berücksichtigen Sie auch den potenziell destruktiven Mehraufwand, der durch die ineffiziente Zuordnung von Datenstrukturen verursacht wird, die jetzt gemarshallt und nicht gemarshallt werden müssen.

Achten Sie abschließend beim Definieren ihrer **HRESULT-Rückgabewerte** darauf, dass Sie keine Fehlercodes erstellen, die mit COM-definierten FACILITY \_ ITF-Codes in Konflikt stehen (Werte zwischen 0x0000 und 0x01FF reserviert sind) oder die mit anderen **HRESULT-Werten** mit demselben Wert in Konflikt stehen. Verwenden Sie nach Möglichkeit die universellen COM-Rückgabewerte für Erfolg und Fehler, und verwenden Sie anstelle eines **HRESULT** einen [**out-Parameter,**](/windows/desktop/Midl/out-idl) um spezifische Informationen für den Funktionsaufruf zurückzugeben.

Weitere Informationen finden Sie in den folgenden Themen:

-   [Entwerfen von Remotable-Schnittstellen](designing-remotable-interfaces.md)
-   [Verwenden einer COM-Schnittstelle](using-a-com-interface.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schnittstellendefinitionen und Typbibliotheken](/windows/desktop/Midl/interface-definitions-and-type-libraries)
</dt> </dl>

 

 