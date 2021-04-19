---
description: Die msiembeddedui-Tabelle definiert eine Benutzeroberfläche, die in das Windows Installer Paket eingebettet ist.
ms.assetid: d4176f99-e819-4b5a-bd06-1a2965891f9a
title: Msiembeddedui-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a52846e88e2d8f3edb439aa6b4a49c99e252173f
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "106361782"
---
# <a name="msiembeddedui-table"></a>Msiembeddedui-Tabelle

Die msiembeddedui-Tabelle definiert eine Benutzeroberfläche, die in das Windows Installer Paket eingebettet ist.

**[Windows Installer 4,0 oder früher](not-supported-in-windows-installer-4-0.md):** Nicht unterstützt. Diese Tabelle ist ab Windows Installer 4,5 verfügbar.

Die msiembeddedui-Tabelle weist die folgenden Spalten auf.



| Spalte        | Typ                               | Schlüssel | Nullwerte zulässig |
|---------------|------------------------------------|-----|----------|
| Msiembeddedui | [Bezeichner](identifier.md)       | J   | N        |
| FileName      | [Text](text.md)                   | N   | N        |
| Attribute    | [Integer](integer.md)             | N   | N        |
| MessageFilter | [Doubleiteger](doubleinteger.md) | N   | J        |
| Daten          | [Binär (Binary)](binary.md)               | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="MsiEmbeddedUI"></span><span id="msiembeddedui"></span><span id="MSIEMBEDDEDUI"></span>Msiembeddedui
</dt> <dd>

Der Primärschlüssel für die Tabelle.

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Einfügen
</dt> <dd>

Der Name der Datei, die die Binär Informationen in der Datenspalte empfängt. Der Name der Datei ist erforderlich, um eine Erweiterung einzuschließen. Beispielsweise ist der Name *embeddedui.dll* akzeptabel, aber *embeddedui* ist nicht akzeptabel. Der Name kann lokalisiert werden. Dieses Feld kann einen kurzen Dateinamen oder einen langen Dateinamen enthalten, kann aber nicht beides enthalten. Das Format dieses Felds ist wie der [Datentyp der Dateiname](filename.md) -Spalte, mit der Ausnahme, dass das vertikale Balken \| Trennzeichen () für die Syntax kurzdateiname/langer Dateiname nicht verfügbar ist. Da bei manchen Webservern die Groß-/Kleinschreibung beachtet werden kann, sollte der Dateiname genau mit der Groß-/Kleinschreibung der Quelldateien übereinstimmen, um

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Legt
</dt> <dd>

Informationen zu den Daten in der Datenspalte. Der Wert in diesem Feld kann eine oder mehrere der folgenden Konstanten enthalten.



| Konstante                      | Hexadezimal | Decimal | Bedeutung                                                                                                                                                                                                                          |
|-------------------------------|-------------|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Keine                          | 0x00        | 0       | Die Datei ist nicht die DLL-Datei für die Benutzeroberfläche. Möglicherweise handelt es sich um eine Ressourcen Datei, die von der Benutzeroberfläche verwendet wird.                                                                                                                       |
| **msidbembeddedui**           | 0x01        | 1       | Die primäre dll-Datei für die Benutzeroberfläche. Es kann nicht mehr als eine Zeile in der Tabelle mit diesem Attribut gekennzeichnet werden. Wenn mehrere Zeilen mit diesem Attribut gekennzeichnet sind, handelt es sich um einen Fehler, und es kann nicht garantiert werden, welche DLL verwendet wird. |
| **msidbembeddecodhandlesbasic** | 0x02        | 2       | Ermöglicht dem Installationsprogramm das Aufrufen der eingebetteten Benutzeroberfläche während einer grundlegenden Installation auf Benutzeroberflächen Ebene. Das Installationsprogramm ignoriert dieses Attribut, wenn es nicht mit dem **msidbembeddedui** -Attribut kombiniert wird.                                         |



 

</dd> <dt>

<span id="MessageFilter"></span><span id="messagefilter"></span><span id="MESSAGEFILTER"></span>MessageFilter
</dt> <dd>

Gibt die Nachrichten Typen an, die an die Benutzeroberflächen-DLL gesendet werden. Diese Spalte ist nur für Zeilen mit dem Attribut **msidbembeddedui** relevant. Dieses Feld sollte NULL sein, wenn eine Zeile auf eine Ressourcen Datei verweist und der Wert von Attributen NULL ist. Wenn eine Zeile auf eine Benutzeroberflächen-DLL verweist, sollte der Wert in dieser Spalte nicht NULL sein.

Der Wert in dieser Spalte kann eine Kombination der folgenden Werte sein. Der Installer ignoriert alle anderen Werte.



| Konstante                           | Hexadezimal | Decimal   | BESCHREIBUNG                                                                                                  |
|------------------------------------|-------------|-----------|--------------------------------------------------------------------------------------------------------------|
| **installlogmode \_ fatalexit**      | 0x00001 beginnt     | 1         | Vorzeitige Beendigung.                                                                                       |
| **installlogmode- \_ Fehler**          | 0x00002     | 2         | Fehlermeldungen                                                                                              |
| **installlogmode- \_ Warnung**        | 0x00004     | 4         | Warnmeldungen.                                                                                            |
| **installlogmode- \_ Benutzer**           | 0x00008     | 8         | Benutzer Nachrichten.                                                                                               |
| **installlogmode- \_ Informationen**           | 0x00010     | 16        | Nicht protokollierte Statusmeldungen.                                                                                    |
| **installlogmode \_ FilesInUse**     | 0x00020     | 32        | Dateien, die derzeit verwendet werden.                                                                                 |
| **installlogmode- \_ ResolveSource**  | 0x00040     | 64        | Anforderungen zur Quell Auflösung.                                                                                  |
| **installlogmode \_ oudedatdiskspace** | 0x00080     | 128       | Speicherplatz Nachrichten.                                                                                         |
| **installlogmode- \_ Aktions Start**    | 0x00100     | 256       | Aktions Start Meldungen.                                                                                       |
| **"installlogmode"- \_ Aktions Daten**     | 0x00200     | 512       | Aktions Datennachrichten.                                                                                        |
| **installlogmode \_ -Status**       | 0x00400     | 1024      | Fortschrittsmeldungen.                                                                                           |
| **installlogmode \_ commondata**     | 0x00800     | 2048      | UI-Initialisierungs Meldungen.                                                                                  |
| **installlogmode \_ initialisieren**     | 0x01000     | 4096      | Beim Starten einer Produktinstallation gesendete Benutzeroberflächen-Start Meldungen.                                            |
| **installlogmode \_ Beenden**      | 0x02000     | 8192      | Nach dem Beenden einer Produktinstallation gesendete Nachrichten für die Benutzeroberfläche.                                         |
| **installlogmode ( \_ Show Dialog)**     | 0x04000     | 16384     | Nachrichten, die vor der Anzeige des UI-Dialog Felds gesendet werden.                                                             |
| **installlogmode \_ rmfilesinuse**   | 0x02000000  | 33554432  | Dateien, die derzeit verwendet werden.                                                                                 |
| **installlogmode- \_ installstart**   | 0x04000000  | 67108864  | Die Installation des Produkts beginnt. Die Meldung enthält ProductName und ProductCode des Produkts.              |
| **installlogmode- \_ installend**     | 0x08000000  | 134217728 | Die Installation von Produkt endet. Die Meldung enthält ProductName, ProductCode und Rückgabewert des Produkts. |



 

</dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>Vorrats
</dt> <dd>

Diese Spalte enthält binäre Informationen. Wenn das Attribut Feld mit dem **msidbembeddedui** -Attribut markiert ist, müssen die Informationen in diesem Feld eine DLL-Datei sein. Wenn das Attribut Feld nicht das Attribut " **msidbembeddedui** " ist, kann es sich bei den Informationen in diesem Feld um eine Ressourcen Datei in einem beliebigen Format handeln.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Um eine eingebettete Benutzeroberfläche zu verwenden, muss der Setup Entwickler diese Funktion im Windows Installer Paket erstellen. Die msiembeddedui-Tabelle definiert die eingebettete Benutzeroberfläche. Die DLL für die eingebettete Benutzeroberfläche sollte die Funktionen " *initializeembeddedui*", " *embeddeduihandler*" und " *shutdownembeddedui* " exportieren. Pakete, die keine eingebettete Benutzeroberfläche unterstützen, können die Windows Installer interne Benutzeroberfläche verwenden.

Um [Debugtools für Windows](https://www.microsoft.com/?ref=go) auf einer eingebetteten Benutzeroberfläche auszuführen, verwenden Sie die in [Debuggen von benutzerdefinierten Aktionen](debugging-custom-actions.md)beschriebenen Verfahren. Legen Sie den Wert von msibreak auf msiembeddedui fest.

Ein Beispiel für eine eingebettete benutzerdefinierte Benutzeroberfläche finden [Sie unter Verwenden einer eingebetteten](using-an-embedded-ui.md)Benutzeroberfläche.

 

 



