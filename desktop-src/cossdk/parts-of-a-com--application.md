---
description: Com+-Anwendungen bestehen aus einer oder mehreren COM-Komponenten.
ms.assetid: e7ed2844-276e-4726-952d-e4d3be2eb6e8
title: Teile einer COM+-Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f75aba454689e25e8706d4a7e3f059d498891f9e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483030"
---
# <a name="parts-of-a-com-application"></a>Teile einer COM+-Anwendung

Com+-Anwendungen bestehen aus einer oder mehreren COM-Komponenten.

Die folgenden Begriffe werden in der com+-Dokumentation verwendet:

<dl> <dt>

<span id="COM_component"></span><span id="com_component"></span><span id="COM_COMPONENT"></span>*COM-Komponente*
</dt> <dd>

Eine binäre Einheit von Code, die COM-Objekte erstellt (einschließlich Paket Erstellung und Registrierungscode).

</dd> <dt>

<span id="COM_object"></span><span id="com_object"></span><span id="COM_OBJECT"></span>*COM-Objekt*
</dt> <dd>

Eine Instanz einer com-Klasse.

</dd> <dt>

<span id="COM_class"></span><span id="com_class"></span><span id="COM_CLASS"></span>*COM-Klasse*
</dt> <dd>

Eine benannte, konkrete Implementierung von einer oder mehreren Schnittstellen. Eine COM-Klasse wird durch eine CLSID identifiziert (manchmal auch durch eine ProgID).

</dd> <dt>

<span id="COM_interface"></span><span id="com_interface"></span><span id="COM_INTERFACE"></span>*COM-Schnittstelle*
</dt> <dd>

Eine Gruppe verwandter Methoden Funktionen, die von einer com-Klasse verfügbar gemacht werden, die einen Vertrag angibt. Dies schließt den Namen, die Schnittstellen Signatur, die Schnittstellen Semantik und das marshallingpufferformat ein. Eine Schnittstelle wird durch eine IID identifiziert. Die Schnittstellen Syntax ist in IDL-und/oder Typbibliotheken definiert. Die Schnittstellen einer com-Klasse sollten in verwaltbare, geschlossene Sätze von Methoden aufgeteilt werden.

COM-Schnittstellen sind unveränderlich. der com-Vertrag besagt, dass Sie nicht geändert werden können. Jede Änderung (z. b. das Hinzufügen von Methoden) erfordert das Definieren einer neuen Schnittstelle

</dd> <dt>

<span id="COM_method"></span><span id="com_method"></span><span id="COM_METHOD"></span>*COM-Methode*
</dt> <dd>

Einer von einer Reihe verwandter Funktionen, die von einer COM-Schnittstelle bereitgestellt werden.

</dd> </dl>

## <a name="configured-and-unconfigured-components"></a>Konfigurierte und nicht konfigurierte Komponenten

Um die von com+-Anwendungen unterstützten Dienste nutzen zu können, erzwingt die com+-Umgebung bestimmte Anforderungen an COM-Komponenten, die für COM+-Anwendungen erstellt wurden. Wenn eine COM-Komponente zu einer COM+-Anwendung hinzugefügt wird, wird Sie als *konfigurierte Komponente* bezeichnet.

COM-Komponenten, die für COM+-Anwendungen erstellt wurden, sind Prozess interne Serverkomponenten. Die Komponente muss eine Typbibliothek (TLB-Datei) enthalten, um alle Klassen zu beschreiben, die in der Komponente implementiert sind, und die Schnittstellen für alle Klassen in der Komponente zu deklarieren. Sie können diese Komponenten mit Microsoft Visual Basic, Microsoft Visual C++ oder einem beliebigen COM-kompatiblen Entwicklungs Tool erstellen und implementieren.

Eine *nicht konfigurierte Komponente* ist eine Komponente, die nicht in einer COM+-Anwendung installiert ist. Sie können die meisten nicht konfigurierten Komponenten in konfigurierte Komponenten transformieren, indem Sie Sie einfach in eine COM+-Anwendung integrieren.

> [!Note]  
> Verwenden Sie nicht die gleiche AppID für eine COM+-Anwendung und in der Registrierung für eine nicht konfigurierte Komponente. Wenn die nicht konfigurierte Komponente aktiviert ist, ruft die Aktivierung möglicherweise die com+-Anwendungsinformationen aus der Registrierung ab, die die für die COM-Aktivierung erforderlichen Informationen nicht enthalten. Ähnliche Probleme können auftreten, wenn ein " [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) " von dllhost aufgerufen wird, der die com+-Server Anwendung hostet.

 

 

 
