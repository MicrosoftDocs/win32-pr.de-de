---
description: Die ReserveCost-Tabelle ist eine optionale Tabelle, mit der der Autor in jedem Verzeichnis, das vom Installationsstatus einer Komponente abhängt, eine Menge Speicherplatz reservieren kann.
ms.assetid: 371e72f1-40a2-4ed2-b0ab-33840075ff47
title: ReserveCost-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5f593fd11789cd2304385b97e96e50a009fbde0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959982"
---
# <a name="reservecost-table"></a>ReserveCost-Tabelle

Die ReserveCost-Tabelle ist eine optionale Tabelle, mit der der Autor in jedem Verzeichnis, das vom Installationsstatus einer Komponente abhängt, eine Menge Speicherplatz reservieren kann.

Die ReserveCost-Tabelle weist die folgenden Spalten auf.



| Spalte        | Typ                               | Schlüssel | Nullwerte zulässig |
|---------------|------------------------------------|-----|----------|
| Reservekey    | [Bezeichner](identifier.md)       | J   | N        |
| Komponente\_   | [Bezeichner](identifier.md)       | N   | N        |
| Reservefolder | [Bezeichner](identifier.md)       | N   | J        |
| Reservelocal  | [Doubleiteger](doubleinteger.md) | N   | N        |
| Reservesource | [Doubleiteger](doubleinteger.md) | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="ReserveKey"></span><span id="reservekey"></span><span id="RESERVEKEY"></span>Reservekey
</dt> <dd>

Primärschlüssel, der einen ReserveCost-Tabelleneintrag eindeutig identifiziert.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Zulieferern\_
</dt> <dd>

Externer Schlüssel für Spalte einer der [Komponenten](component-table.md) Tabellen. Reserviert eine angegebene Menge an Speicherplatz, wenn diese Komponente installiert werden soll.

</dd> <dt>

<span id="ReserveFolder"></span><span id="reservefolder"></span><span id="RESERVEFOLDER"></span>Reservefolder
</dt> <dd>

Diese Spalte enthält den Namen einer Eigenschaft, bei der es sich um den vollständigen Pfad zum Zielverzeichnis handelt. Dieser Eigenschaftsname ist in der Regel der Name eines Verzeichnisses in der [Verzeichnis](directory-table.md) Tabelle oder der Name eines Eigenschaften Satzes, der mithilfe der [AppSearch](appsearch-action.md) -Aktion abgerufen wurde. Dadurch wird die Menge des Speicherplatzes, der in reservelocal oder reservesource angegeben ist, den volumekosten des Geräts hinzugefügt, das das Verzeichnis enthält.

</dd> <dt>

<span id="ReserveLocal"></span><span id="reservelocal"></span><span id="RESERVELOCAL"></span>Reservelocal
</dt> <dd>

Die Anzahl der Bytes an Speicherplatz, die reserviert werden sollen, wenn die verknüpfte Komponente zur lokalen Installation installiert wird.

</dd> <dt>

<span id="ReserveSource"></span><span id="reservesource"></span><span id="RESERVESOURCE"></span>Reservesource
</dt> <dd>

Die Anzahl der Bytes an Speicherplatz, die reserviert werden sollen, wenn die verknüpfte Komponente zum Ausführen von der Quelle installiert wird.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Reservierung von Kosten auf diese Weise kann für Autoren nützlich sein, die sicherstellen möchten, dass nach Abschluss der Installation ein Minimum an Speicherplatz verfügbar ist. Beispielsweise kann dieser Speicherplatz für Benutzer Dokumente oder Anwendungs Dateien (z. b. Indexdateien) reserviert werden, die erst erstellt werden, nachdem die Anwendung nach der Installation gestartet wurde.

Mithilfe der Tabelle ReserveCost können Sie benutzerdefinierte Aktionen verwenden, um die ungefähren Kosten für beliebige Dateien, Registrierungseinträge oder andere Elemente anzugeben, die von der benutzerdefinierten Aktion installiert werden könnten. Benutzerdefinierte Aktionen, die der ReserveCost-Tabelle Einträge hinzufügen, sollten zwischen den Aktionen " [costinitialize](costinitialize-action.md) " und " [filecost](filecost-action.md) " sequenziert werden. Dies ist erforderlich, damit die filecost-Aktion die Kosten aller von Einträgen in der ReserveCost-Tabelle betroffenen Komponenten ordnungsgemäß initialisieren kann.

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 



