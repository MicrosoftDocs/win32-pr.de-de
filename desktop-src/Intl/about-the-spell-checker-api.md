---
description: Für Benutzer auf der ganzen Welt ist die Texteingabe Teil eines modernen Computer Erlebnisses, für Blogs, Kommentare, Tweets, Instant Messaging oder andere Arten von Texteingaben. In Windows 8 ist die Rechtschreibprüfung integriert, um Steuerelemente zu bearbeiten.
ms.assetid: ED569D4F-568B-4381-91C3-8EAEDA4DD47C
title: Informationen zur Rechtschreibprüfungs-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f0d356823e665781052e2a2d5ea98b358155038
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866375"
---
# <a name="about-the-spell-checking-api"></a>Informationen zur Rechtschreibprüfungs-API

Für Benutzer auf der ganzen Welt ist die Texteingabe Teil eines modernen Computer Erlebnisses, für Blogs, Kommentare, Tweets, Instant Messaging oder andere Arten von Texteingaben. In Windows 8 ist die Rechtschreibprüfung integriert, um Steuerelemente zu bearbeiten.

Entwickler können die Rechtschreibprüfungs-API in ihren Apps verwenden, um verfügbare Rechtschreib Überprüfungs Dienste zu nutzen. Entwickler können auch Rechtschreibprüfungen erstellen, die zu Anbietern werden und in das Windows-Rechtschreib Prüfungs Framework integriert sind.

Die Rechtschreibprüfungs-API ist für die Verwendung durch professionelle C/C++-Entwickler von Windows Component Object Model-Apps (com) konzipiert. Die Rechtschreibprüfungs-API wird nicht für die Verwendung in einem Windows-oder ASP.net-Dienst unterstützt.

## <a name="versioning"></a>Versionskontrolle

Die Rechtschreibprüfungs-API ist ab Windows 8 oder Windows Server 2012 verfügbar. Zukünftige Ergänzungen der API werden durch das Erstellen neuer Schnittstellen behandelt, die mithilfe von [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) auf den vorhandenen festgelegt werden können.

## <a name="interfaces"></a>Schnittstellen

Alle Schnittstellen müssen freigegeben werden, wenn Sie nicht mehr verwendet werden. Alle zurückgegebenen **LPWSTR** -Zeichen folgen (und **lpolestr** -Elemente aus [**IEnumString**](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring)) müssen mit " [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) " freigegeben werden, wenn Sie nicht mehr verwendet werden.

## <a name="error-handling"></a>Fehlerbehandlung

Fehler werden als **HRESULT** s zurückgegeben. [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) und [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) werden in dieser API nicht unterstützt. Fehler können mit Ausnahme falscher Argumente nicht besonders handlungsfähig sein.

Standard-RPC-Fehlercodes können von jedem API-Aufruf zurückgegeben werden, da Sie außerhalb des Prozesses sind. Es gelten Standard-RPC-Timeouts.

## <a name="security"></a>Sicherheit

Die Rechtschreibprüfungs-API lädt möglicherweise externen Code (Rechtschreibprüfung-Anbieter). Dieser Code wird außerhalb der proc-Prozedur und in einem eingeschränkten Sicherheitskontext ausgeführt.

## <a name="dictionary-files"></a>Wörterbuchdateien

Die benutzerspezifischen Wörterbücher für eine Sprache, die den Inhalt der hinzugefügten, ausgeschlossenen und automatisch korrekten Wortlisten enthalten, befinden sich unter% APPDATA% \\ Microsoft \\ Spelling \\ *<language tag>* . Die Dateinamen sind Default. dic (Added), Default. exc (ausgeschlossen) und default. ACL (AutoCorrect). Die Dateien sind UTF-16-Le-Klartext, das mit der entsprechenden Byte Reihenfolge Markierung (BOM) beginnen muss. Jede Zeile enthält ein Wort (in der Liste hinzugefügter und ausgeschlossener Wörter) oder ein Auto korrektes Paar mit den Wörtern, die durch einen senkrechten Strich (" \| ") getrennt sind (in der Liste der AutoKorrektur-Wörter). Andere im Verzeichnis vorhandene. dic-, EXC-und ACL-Dateien werden vom Rechtschreib Überprüfungs Dienst erkannt und den Benutzer Wortlisten hinzugefügt. Diese Dateien gelten als schreibgeschützt und werden nicht durch die Rechtschreibprüfungs-API geändert.

## <a name="installing-a-spell-checking-provider"></a>Installieren eines Rechtschreib Prüfungs Anbieters

Bei der Installation eines Rechtschreib Prüfungs Anbieters müssen alle verwendeten Dateien an einem Speicherort abgelegt werden, der Lesezugriff auf die sid ([Sicherheits](../secauthz/security-identifiers.md)-ID) "alle Anwendungspakete" zulässt. Die Installation in einem Ordner unter "Programmdateien" funktioniert gut. Außerdem muss der Anbieter einige Schlüssel in der Registrierung festlegen, damit er für die Rechtschreibprüfungs-API angezeigt wird. Dies kann entweder in der HKEY \_ Current User-Struktur \_ oder in der HKEY \_ Local Machine Hive erfolgen, \_ je nachdem, ob Sie nur für den aktuellen Benutzer oder für alle Benutzer installiert werden soll.


```
Key: <Registry hive>\SOFTWARE\Classes\CLSID\<Server CLSID>
     Default (REG_SZ) = <Name of the provider>

Key: <Registry hive>\SOFTWARE\Classes\CLSID\<Server CLSID>\InprocServer32
     ThreadingModel (REG_SZ) = "Both"

Key: <Registry hive>\SOFTWARE\Classes\CLSID\<Server CLSID>\Version
     Version (REG_SZ) = <Version>

Key: <Registry hive>\SOFTWARE\Microsoft\Spelling\Spellers\<Provider id string>
     CLSID (REG_SZ) = <CLSID of the COM Server that implements the provider>
```



Das Beispiel für den [Rechtschreib Prüfungs Anbieter](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SpellCheckerProvider) enthält ein Beispiel für die Registrierung, die zum Installieren eines Anbieters erforderlich ist.

Wenn Sie neue Optionen für die Rechtschreibprüfung für einen Rechtschreibprüfungs-Anbieter erstellen, finden Sie unter [**ioptiondescription:: ID**](/windows/desktop/api/Spellcheck/nf-spellcheck-ioptiondescription-get_id) Hinweise zum benennen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[API-Referenz zur Rechtschreibprüfung](spell-checker-api-reference.md)
</dt> <dt>

[Beispiel für Rechtschreibprüfung (Client)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SpellCheckerClient)
</dt> <dt>

[Beispiel für Rechtschreib Prüfungs Anbieter](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SpellCheckerProvider)
</dt> <dt>

[**Ioptiondescription:: ID**](/windows/desktop/api/Spellcheck/nf-spellcheck-ioptiondescription-get_id)
</dt> <dt>

[**IEnumString**](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring)
</dt> <dt>

[**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))
</dt> </dl>

 

 
