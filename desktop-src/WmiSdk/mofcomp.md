---
description: Der MOF-Compiler (Managed Object Format) analysiert eine Datei, die MOF-Anweisungen enthält, und fügt die Klassen und Klassen Instanzen, die in der Datei definiert sind, dem WMI-Repository hinzu.
ms.assetid: 9858da09-fb91-43a4-9817-83b10e2ee08f
ms.tgt_platform: multiple
title: Mofcomp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da63525e4bb8a32f3628b68295e5cc8ade0b08de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863324"
---
# <a name="mofcomp"></a>Mofcomp

Der [*MOF-Compiler (Managed Object Format)*](gloss-m.md) analysiert eine Datei, die MOF-Anweisungen enthält, und fügt die Klassen und Klassen Instanzen, die in der Datei definiert sind, dem WMI-Repository hinzu. MOF-Dateien werden normalerweise während der Installation der Systeme, mit denen Sie bereitgestellt werden, automatisch kompiliert, aber Sie können MOF-Dateien auch mit diesem Tool kompilieren.

Weitere Informationen zum Suchen und Verwenden von mofcomp.exe finden [Sie unter Verwenden von WMI-Verwaltungs Tools](/previous-versions/system-center/configuration-manager-2003/cc180468(v=technet.10)). Weitere Informationen zum Entfernen von Klassen und Instanzen aus dem WMI-Repository finden Sie im [**pragma deleteclass**](pragma-deleteclass.md) -Präprozessorbefehl.

Im folgenden Codebeispiel wird gezeigt, wie der MOF-Compiler für eine Datei ausgeführt wird.

``` syntax
mofcomp
  [-autorecover]
  [-check]
  [-N:<namespacepath>]
  [-class:createonly | -class:forceupdate | 
   -class:safeupdate | -class:updateonly ] 
  [-instance:updateonly | -instance:createonly]
  [-B:<filename>]
  [-WMI]
  [-P:<Password>]
  [-U:<UserName>]
  [-A:<Authority>]
  [-MOF:<path>] 
  [-MFL:<path>] 
  [-AMENDMENT:<Locale>]
  [-ER:<ResourceName>]
  [-L:<ResourceLocale>] 
  <MOFfile>
```

## <a name="switches"></a>Switches

<dl> <dt>

<span id="-autorecover"></span><span id="-AUTORECOVER"></span>**-AutoRecover**
</dt> <dd>

Fügt die benannte MOF-Datei zur Liste der Dateien hinzu, die während der Wiederherstellung des Repository kompiliert wurden. Die Liste der Auto Wiederherstellen-MOF-Dateien wird im Registrierungsschlüssel gespeichert:

**HKEY \_ Software für den lokalen \_ Computer** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM \\**

Die in diesem Registrierungs Eintrag aufgeführten MOF-Dateien müssen sich auf dem lokalen Computer befinden, da MOF-Dateien, die den **Auto Wiederherstellen** -Befehl verwenden, keine MOF-Dateien wiederherstellen können, die sich auf einem Remote Computer befinden

> [!Note]  
> Um sicherzustellen, dass alle ihre WMI-Klassendefinitionen für verwaltete Objekte im [*WMI-Repository*](gloss-w.md) wieder hergestellt werden, wenn WMI einen Fehler aufweist und neu gestartet wird, verwenden Sie die " [**\# pragma Auto Wiederherstellen**](pragma-autorecover.md) "-Präprozessoranweisung in der MOF-Datei ( [*Managed Object Format*](gloss-m.md) ).

 

</dd> <dt>

<span id="-check"></span><span id="-CHECK"></span>**-Überprüfen**
</dt> <dd>

Fordert an, dass der Compiler eine Syntax nur überprüft und entsprechende Fehlermeldungen druckt. Mit diesem Schalter kann kein anderer Switch verwendet werden. Bei Verwendung dieses Schalters wird keine Verbindung mit Windows-Verwaltungsinstrumentation (WMI) hergestellt, und es werden keine Änderungen am WMI-Repository vorgenommen.

</dd> <dt>

<span id="-N__namespacepath_"></span><span id="-n__namespacepath_"></span><span id="-N__NAMESPACEPATH_"></span>**-N: <** _Wert von NamespacePath_*_>_*
</dt> <dd>Fordert an, dass der Compiler die MOF-Datei in den Namespace lädt, der als *Wert von NamespacePath* angegeben ist. Das kompilierte MOF wird in den Standard-Standard Namespace "Standard" geladen, \\ sofern dieser Schalter nicht verwendet wird. Sie können auch den **\# pragma-Namespace** des Präprozessorbefehls ("_Namespace Pfad_*_")_* in der MOF-Datei einfügen, um denselben Effekt zu erzielen. Wenn sowohl der **-N: Switch-** als auch der \# <a href="pragma-namespace.md">pragma-Namespace</a> -Befehl verwendet werden, hat der \# **pragma-Namespace** **Auto Wiederherstellen** Priorität. In diesem Fall besteht die einzige Möglichkeit zum Kompilieren der MOF-Datei in einen anderen Namespace darin, die MOF-Datei zu bearbeiten und den \# **pragma-Namespace** -Befehl zu ändern. Ein Remote Computer kann mithilfe von \\ \\ MachineName root default angegeben werden \\ \\ .</dd> <dt>

<span id="-class_createonly"></span><span id="-CLASS_CREATEONLY"></span>**-Klasse: "kreateonly"**
</dt> <dd>

Fordert an, dass der Compiler keine Änderungen an vorhandenen Klassen vornimmt. Wenn dieser Schalter verwendet wird, wird der Kompilierungs Vorgang beendet, wenn eine in der MOF-Datei angegebene Klasse bereits vorhanden ist.

</dd> <dt>

<span id="-class_forceupdate"></span><span id="-CLASS_FORCEUPDATE"></span>**-Class: ForceUpdate**
</dt> <dd>

Erzwingt das Aktualisieren von Klassen, wenn widersprüchliche untergeordnete Klassen vorhanden sind. Angenommen, ein Klassen Qualifizierer ist in einer untergeordneten Klasse definiert, und die Basisklasse versucht, denselben Qualifizierer hinzuzufügen. In **-Class: der ForceUpdate** -Modus löst der MOF-Compiler diesen Konflikt durch Löschen des in Konflikt stehenden Qualifizierers in der untergeordneten Klasse auf. Wenn die untergeordnete Klasse über Instanzen verfügt, schlägt das erzwungene Update fehl.

</dd> <dt>

<span id="-class_safeupdate"></span><span id="-CLASS_SAFEUPDATE"></span>**-Klasse: safeupdate**
</dt> <dd>

Ermöglicht das Aktualisieren von Klassen auch dann, wenn untergeordnete Klassen vorhanden sind, solange die Änderung keine Konflikte mit untergeordneten Klassen verursacht. Dieses Flag ermöglicht beispielsweise das Hinzufügen einer neuen Eigenschaft zur Basisklasse, die nicht zuvor in untergeordneten Klassen erwähnt wurde. Wenn die untergeordneten Klassen Instanzen aufweisen, schlägt die Aktualisierung fehl.

</dd> <dt>

<span id="-class_updateonly"></span><span id="-CLASS_UPDATEONLY"></span>**-Klasse: updateonly**
</dt> <dd>

Fordert an, dass der Compiler keine neuen Klassen erstellt. Wenn dieser Schalter verwendet wird, wird der Kompilierungs Vorgang beendet, wenn keine in der MOF-Datei angegebene Klasse vorhanden ist.

</dd> <dt>

<span id="-instance_updateonly"></span><span id="-INSTANCE_UPDATEONLY"></span>**-Instanz: updateonly**
</dt> <dd>

Fordert an, dass der Compiler keine neuen Instanzen erstellt. Wenn dieser Schalter verwendet wird, wird der Kompilierungs Vorgang beendet, wenn keine in der MOF-Datei angegebene Instanz vorhanden ist.

</dd> <dt>

<span id="-instance_createonly"></span><span id="-INSTANCE_CREATEONLY"></span>**-instance: "kreateonly"**
</dt> <dd>

Fordert an, dass der Compiler keine Änderungen an vorhandenen Instanzen vornimmt. Wenn dieser Schalter verwendet wird, wird der Kompilierungs Vorgang beendet, wenn eine in der MOF-Datei angegebene Instanz bereits vorhanden ist.

</dd> <dt>

<span id="-B__filename_"></span><span id="-b__filename_"></span><span id="-B__FILENAME_"></span>**-B: <** _Dateiname_*_>_*
</dt> <dd>

Fordert an, dass der Compiler eine binäre Version der MOF-Datei mit dem Namen *filename* erstellt, ohne Änderungen am WMI-Repository vorzunehmen.

Wenn Sie die Option **-B: <** _filename_ verwenden, *_>_* um eine binäre MOF-Datei zu erstellen, werden nur standardmäßige qualifizierervarianten im WMI-Repository gespeichert.

Das binäre MOF-Format ist das zwischen Format für die Kombination eines WDM-Treibers mit dem MOF als Ressource. Die binäre MOF stellt Klassen und Instanzen wie eine MOF-Datei des Texts dar und wird komprimiert, bevor Sie auf dem Datenträger gespeichert wird.

</dd> <dt>

<span id="-WMI"></span><span id="-wmi"></span>**-WMI**
</dt> <dd>

Fordert an, dass der Compiler eine WMI-Syntax Überprüfung ausführt. Der Schalter **-B:** muss mit diesem Switch verwendet werden. Der **-WMI-** Schalter wird nur zum entwickeln binärer MOF-Dateien verwendet, die von WDM-Gerätetreibern verwendet werden. Dieser Schalter Ruft eine separate binäre MOF-Datei Prüfung auf, die ausgeführt wird, nachdem die binäre MOF-Datei erstellt wurde.

</dd> <dt>

<span id="-P__Password_"></span><span id="-p__password_"></span><span id="-P__PASSWORD_"></span>**-P: <** _Kennwort_*_>_*
</dt> <dd>

Gibt *das Kennwort* als Kennwort für den Computerbenutzer an, das bei der Anmeldung eingegeben werden soll.

</dd> <dt>

<span id="-U__UserName_"></span><span id="-u__username_"></span><span id="-U__USERNAME_"></span>**-U: <** _Benutzername_*_>_*
</dt> <dd>

Gibt den *Benutzer* Namen als Namen des Benutzers an, der sich anmeldet.

</dd> <dt>

<span id="-A__Authority_"></span><span id="-a__authority_"></span><span id="-A__AUTHORITY_"></span>**-A: <** _Autorität_*_>_*
</dt> <dd>

Gibt die *Autorität* als Autorität (Domänen Name) an, die bei der Anmeldung bei WMI verwendet werden soll.

</dd> <dt>

<span id="-MOF__path_"></span><span id="-mof__path_"></span><span id="-MOF__PATH_"></span>**-MOF: <** _Pfad_*_>_*
</dt> <dd>

Der Name der sprach neutralen Ausgabe. Wird mit dem Switch **--Zusatz** verwendet, um den Namen der sprach neutralen MOF-Datei anzugeben, die generiert werden soll.

</dd> <dt>

<span id="-MFL__path_"></span><span id="-mfl__path_"></span><span id="-MFL__PATH_"></span>**-MFL: <** _Pfad_*_>_*
</dt> <dd>

Der Name der sprachspezifischen Ausgabe. Wird mit dem Switch **--Zusatz** verwendet, um den Namen der sprachspezifischen MOF-Datei anzugeben, die generiert werden soll.

</dd> <dt>

<span id="-AMENDMENT__Locale_"></span><span id="-amendment__locale_"></span><span id="-AMENDMENT__LOCALE_"></span>**-Zusatz: <**  Gebiets Schema *_>_*
</dt> <dd>

Teilt die MOF-Datei in sprachneutrale und spezifische Versionen auf. Der MOF-Compiler erstellt eine sprachneutrale Form der MOF-Datei, für die alle geänderten Qualifizierer entfernt wurden. Außerdem wird eine lokalisierte Version der MOF-Datei mit einer MFL-Dateinamenerweiterung erstellt. Der *locale* -Parameter gibt den Namen des untergeordneten Namespace an, der die lokalisierten Klassendefinitionen enthält. Das Format des *locale* -Parameters ist MS \_ xxx, wobei xxx der hexadezimale Wert der Windows-LCID ist. Beispielsweise ist das Gebiets Schema für amerikanisches Englisch MS \_ 409.

</dd> <dt>

<span id="-ER__ResourceName_"></span><span id="-er__resourcename_"></span><span id="-ER__RESOURCENAME_"></span>**-Er <** _resourceName_*_>_*
</dt> <dd>

Extrahiert binäres MOF aus einer benannten Ressource. Mit diesem Switch wird die binäre MOF-Datei aus der-Klasse im WMI-Repository abgerufen, während der-B-Switch das binäre MOF-Format aus einer MOF-Datei erstellt.

</dd> <dt>

<span id="-L__ResourceLocale_"></span><span id="-l__resourcelocale_"></span><span id="-L__RESOURCELOCALE_"></span>**-L: <** _resourcelocale_*_>_*
</dt> <dd>

Dies ist optional. Extrahiert die lokalisierten MOF-Beschreibungen aus der binären MOF-Datei, wenn Sie mit dem Schalter-er verwendet wird

</dd> <dt>

<span id="_MOFfile_"></span><span id="_moffile_"></span><span id="_MOFFILE_"></span>**<**_Die_*_>_*
</dt> <dd>

Der Name der Datei, die analysiert werden soll.

</dd> </dl>

## <a name="return-values"></a>Rückgabewerte

Beim ersten Vorgang führt der MOF-Compiler eine Syntax Überprüfung für die MOF-Datei aus. Wenn der Compiler Fehler findet, wird eine Fehlermeldung ausgegeben, und der Prozess wird beendet.

Der MOF-Compiler kann die folgenden Werte zurückgeben:

<dl> <dt>

<span id="0"></span>0
</dt> <dd>

Der MOF-Kompilierungs Vorgang war erfolgreich.

</dd> <dt>

<span id="1"></span>1
</dt> <dd>

Der MOF-Compiler konnte keine Verbindung mit dem WMI-Server herstellen. Dies ist entweder auf einen Semantik Fehler, wie z. b. eine Inkompatibilität mit dem vorhandenen WMI-Repository oder ein tatsächlicher Fehler, wie z. b. das Starten des WMI-Servers.

</dd> <dt>

<span id="2"></span>2
</dt> <dd>

Mindestens ein Befehls Zeilenschalter war ungültig.

</dd> <dt>

<span id="3"></span>€
</dt> <dd>

Ein MOF-Syntax Fehler ist aufgetreten.

</dd> </dl>

Wenn die MOF-Datei ordnungsgemäß analysiert wird, aber versucht wird, einen Vorgang auszuführen, der durch einen Befehls Zeilenschalter unzulässig ist, gibt der Compiler einen Fehlercode zurück, der von WMI generiert wurde, und nicht die Rückgabecodes, die in der obigen Liste aufgeführt sind. Beispielsweise wird ein WMI-Fehlercode zurückgegeben, wenn der Schalter **-instance: updateonly** angegeben wird und die MOF-Datei versucht, eine Instanz zu erstellen.

Wenn die [**\# pragma Auto Wiederherstellen**](pragma-autorecover.md) -Präprozessoranweisung nicht in der Datei enthalten ist, wird die folgende Warnung zurückgegeben:

``` syntax
WARNING: FileYourMof.Mof does not contain #PRAGMA AUTORECOVER.
If the WMI repository is rebuilt in the future, the contents of this 
MOF file   will not be included in the new WMI repository.
To include this MOF file when the WMI Repository is automatically 
reconstructed, place the #PRAGMA AUTORECOVER statement on the first 
line of the MOF file.
```

## <a name="remarks"></a>Bemerkungen

Der MOF-Compiler ist im Verzeichnis% windir% \\ system32 \\ WBEM verfügbar. Sie müssen die MOF-Datei als Parameter des MOF-Compilers angeben. Sie können auch einen AutoRecover-Schalter angeben, wenn die MOF-Datei automatisch erneut kompiliert werden soll, wenn das CIM-Repository jemals automatisch wieder hergestellt werden muss. Wenn Sie weitere Informationen erhalten, geben Sie " **MUF Comp/?** an der Eingabeaufforderung ein.

Eine MOF-Datei, die den Unicode-Zeichensatz verwendet, enthält eine Signatur als die ersten zwei Bytes der Datei. Diese Signatur ist entweder u + FFFE oder u + FEFF, abhängig von der Byte Reihenfolge der Datei.

Wenn beim Analyse-Prozess keine Fehler auftreten, stellt der MOF-Compiler eine Verbindung mit dem WMI-Server her, der auf dem lokalen Computer ausgeführt wird, es sei denn, der Schalter **-Check** ist angegeben Klassen und Instanzen, die in der MOF-Datei definiert sind, werden dem WMI-Repository hinzugefügt.

Wenn beim Aktualisieren des WMI-Repository ein Fehler auftritt, versucht der Compiler nicht, das Repository in seinen Zustand zurückzusetzen, bevor der Compiler mit der Verarbeitung begonnen hat.

**Windows 8:** Bei der Installation eines Anbieters behandelt "MUF Comp" die \[ Schlüssel \] -und \[ statischen \] Qualifizierer unabhängig von ihren tatsächlichen Werten als "true", wenn Sie vorhanden sind. Andere Qualifizierer werden als false behandelt, wenn Sie vorhanden sind, aber nicht explizit auf true festgelegt sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**pragma-Namespace**](pragma-namespace.md)
</dt> <dt>

[Kompilieren von MOF-Dateien](compiling-mof-files.md)
</dt> <dt>

[Kompilieren lokalisierter MOF-Dateien](compiling-localized-mof-files.md)
</dt> <dt>

[Registrieren eines Anbieters](registering-a-provider.md)
</dt> <dt>

[**Imufcompiler:: CompileFile**](/windows/desktop/api/Wbemcli/nf-wbemcli-imofcompiler-compilefile)
</dt> </dl>

 

