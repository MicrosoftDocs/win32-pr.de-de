---
description: Ein Assemblymanifest ist eine XML-Datei, die eine nebenseitige Assembly beschreibt.
ms.assetid: f7973019-0a80-498e-adf1-c66267c813f4
title: Assemblymanifeste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5d7c6739bc83e56a42a926ca6aecb739fc41bbf39225cc531afc7afc6706ccc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142513"
---
# <a name="assembly-manifests"></a>Assemblymanifeste

Ein Assemblymanifest ist eine XML-Datei, die eine nebenseitige Assembly beschreibt. Assemblymanifeste beschreiben die Namen und Versionen von nebenseitigen Assemblys, Dateien und Ressourcen der Assembly sowie die Abhängigkeit der Assembly von anderen nebeneinander verfügbaren Assemblys. Die richtige Installation, Aktivierung und Ausführung von nebeneinander ausgeführten Assemblys erfordert, dass das Assemblymanifest immer eine Assembly im System begleitet.

Eine vollständige Liste des XML-Schemas finden Sie unter [Manifestdateischema](manifest-file-schema.md).

Assemblymanifesten verfügen über die folgenden Elemente und Attribute.



| Element                           | Attribute                | Erforderlich |
|-----------------------------------|---------------------------|----------|
| **Versammlung**                      |                           | Ja      |
|                                   | **manifestVersion**       | Ja      |
| **noInheritable**                 |                           | Nein       |
| **Assemblyidentity**              |                           | Ja      |
|                                   | **type**                  | Ja      |
|                                   | **name**                  | Ja      |
|                                   | **language**              | Nein       |
|                                   | **processorArchitecture** | Nein       |
|                                   | **version**               | Ja      |
|                                   | **Publickeytoken**        | Nein       |
| **Abhängigkeit**                    |                           | Nein       |
| **Dependentassembly**             |                           | Nein       |
| **datei**                          |                           | Nein       |
|                                   | **name**                  | Ja      |
|                                   | **Hashalg**               | Nein       |
|                                   | **hash**                  | Nein       |
| **comClass**                      |                           | Nein       |
|                                   | **description**           | Nein       |
|                                   | **Clsid**                 | Ja      |
|                                   | **threadingModel**        | Nein       |
|                                   | **tlbid**                 | Nein       |
|                                   | **Progid**                | Nein       |
|                                   | **miscStatus**            | Nein       |
|                                   | **miscStatusIcon**        | Nein       |
|                                   | **miscStatusContent**     | Nein       |
|                                   | **miscStatusDocPrint**    | Nein       |
|                                   | **miscStatusDocPrint**    | Nein       |
| **Typelib**                       |                           | Nein       |
|                                   | **tlbid**                 | Ja      |
|                                   | **version**               | Ja      |
|                                   | **helpdir**               | Ja      |
|                                   | **Resourceid**            | Nein       |
|                                   | **flags**                 | Nein       |
| **comInterfaceExternalProxyStub** |                           | Nein       |
|                                   | **Iid**                   | Ja      |
|                                   | **baseInterface**         | Nein       |
|                                   | **numMethods**            | Nein       |
|                                   | **name**                  | Nein       |
|                                   | **tlbid**                 | Nein       |
|                                   | **proxyStubClsid32**      | Nein       |
| **comInterfaceProxyStub**         |                           | Nein       |
|                                   | **Iid**                   | Ja      |
|                                   | **name**                  | Ja      |
|                                   | **tlbid**                 | Nein       |
|                                   | **baseInterface**         | Nein       |
|                                   | **numMethods**            | Nein       |
|                                   | **proxyStubClsid32**      | Nein       |
|                                   | **threadingModel**        | Nein       |
| **windowClass**                   |                           | Nein       |
|                                   | **Versionierte**             | Nein       |



 

## <a name="file-location"></a>Speicherort

Assemblymanifeste können an drei Speicherorten installiert werden:

-   Als Manifeste, die [freigegebene Assemblys](/windows/desktop/Msi/shared-assemblies)begleitet, sollten Assemblymanifeste als separate Datei im parallelen Assemblycache installiert werden. Dies ist normalerweise der WinSxS-Ordner im Windows Verzeichnis.
-   Als Manifeste, die [private Assemblys](/windows/desktop/Msi/private-assemblies)begleitet, sollten Assemblymanifeste in der Verzeichnisstruktur der Anwendung installiert werden. Dies ist in der Regel eine separate Datei im selben Ordner wie die ausführbare Datei der Anwendung.
-   Als Ressource in einer DLL ist die Assembly für die private Verwendung der DLL verfügbar. Ein Assemblymanifest kann nicht als Ressource in eine EXE-Datei eingeschlossen werden. Eine EXE-Datei kann ein [Anwendungsmanifest](application-manifests.md) als Ressource enthalten.

## <a name="file-name-syntax"></a>Dateinamensyntax

Der Name eines Assemblymanifests ist ein beliebiger gültiger Dateiname gefolgt von .manifest.

Beispielsweise würde ein Assemblymanifest, das auf myassembly verweist, die folgende Dateinamenssyntax verwenden. Sie können die <*Ressourcen-ID*> Feld weglassen, wenn das Assemblymanifest als separate Datei installiert wird oder wenn die Ressourcen-ID 1 ist.

<dl> myassembly. <resource ID> . Manifest
</dl>

> [!Note]  
> Aufgrund der Art und Weise, wie nebeneinander nach privaten Assemblys gesucht wird, gelten beim Packen einer DLL als private Assembly die folgenden Namenseinschränkungen. Eine empfohlene Vorgehensweise besteht darin, das Assemblymanifest als Ressource in die DLL zu integrieren. In diesem Fall muss die Ressourcen-ID gleich 1 sein, und der Name der privaten Assembly kann mit dem Namen der DLL übereinstimmen. Wenn der Name der DLL beispielsweise Microsoft.Windows.mysample.dll ist, kann der Wert des namensattributs, das im **assemblyIdentity-Element** des Manifests verwendet wird, auch Microsoft sein. Windows.mysample. Eine alternative Möglichkeit besteht darin, das Assemblymanifest in einer separaten Datei zu speichern. In diesem Fall müssen sich der Name der Assembly und ihr Manifest vom Namen der DLL unterscheiden. Beispiel: Microsoft. Windows.mysampleAsm, Microsoft. Windows.mysampleAsm.manifest und Microsoft.Windows.Mysample.dll. Weitere Informationen dazu, wie nebeneinander nach privaten Assemblys sucht, finden Sie unter [Assemblysuchsequenz.](assembly-searching-sequence.md)

 

## <a name="elements"></a>Elemente

Bei Namen von Elementen und Attributen wird die Groß-/Kleinschreibung beachtet. Bei den Werten von Elementen und Attributen wird die Groß-/Kleinschreibung mit Ausnahme des Werts des Typattributs nicht beachtet.

<dl> <dt>

<span id="assembly"></span><span id="ASSEMBLY"></span>**Versammlung**
</dt> <dd>

Ein Containerelement. Das erste Unterelement muss ein **assemblyIdentity-** oder **noInheritable-Element** sein. Das Assemblymanifest beschreibt eindeutig die durch **assemblyIdentity** identifizierte assembly-seitige Assembly. Erforderlich.

Das Assemblyelement muss sich im Namespace "urn:schemas-microsoft-com:asm.v1" befinden. Untergeordnete Elemente der Assembly müssen sich ebenfalls in diesem Namespace befinden, entweder durch Vererbung oder durch Tagging.

Das **Assemblyelement** weist das folgende Attribut auf.



| attribute           | Beschreibung                                           |
|---------------------|-------------------------------------------------------|
| **manifestVersion** | Das **manifestVersion-Attribut** muss auf 1.0 festgelegt werden. |



 

</dd> <dt>

<span id="noInheritable"></span><span id="noinheritable"></span><span id="NOINHERITABLE"></span>**noInheritable**
</dt> <dd>

Schließen Sie dieses Element in ein Assemblymanifest ein, um anzugeben, dass die Assembly die [Aktivierungskontexte](activation-contexts.md) und ihre Objekte verwaltet. Das **noInheritable-Element** muss ein Unterelement eines **Assemblyelements** sein. Das **assemblyIdentity-Element** sollte nach jedem **noInheritable-Element** folgen. Das **noInheritable-Element** ist im Assemblymanifest erforderlich, wenn die Assembly von [Anwendungsmanifesten](application-manifests.md) verwendet wird, die das **noInherit-Element** enthalten. Ein **noInheritable-Element** in einem Anwendungsmanifest hat keine Auswirkungen. Ein **noInheritable-Element** verfügt über keine untergeordneten Elemente.

</dd> <dt>

<span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>**Assemblyidentity**
</dt> <dd>

Beschreibt eine -Assembly und identifiziert sie eindeutig.

Als erstes Unterelement eines **Assemblyelements** beschreibt **assemblyIdentity** die side-by-side-Assembly, die dieses Assemblymanifest besitzt, und identifiziert sie eindeutig. Dies wird als DEF-context **assemblyIdentity** des Assemblymanifests bezeichnet.

Als erstes Unterelement eines **dependentAssembly-Elements** beschreibt **assemblyIdentity** eine von der DEF-Kontextassemblyidentity verwendete Assembly und identifiziert sie eindeutig. Dies wird als **REF-KontextassemblyIdentität** des Assemblymanifests bezeichnet. Die DEF-Kontextassembly erfordert, dass die REF-Kontextassembly ordnungsgemäß funktioniert. Beachten Sie, dass jede REF-context **assemblyIdentity** genau mit einer entsprechenden DEF-context **assemblyIdentity** im eigenen Assemblymanifest der Referenzassembly übereinstimmen muss.

Dieses Element verfügt über keine Unterelemente. Das **assemblyIdentity-Element** verfügt über die folgenden Attribute.



| attribute                 | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **type**                  | Gibt den Assemblytyp an. Der Wert muss win32 und in Kleinbuchstaben sein. Erforderlich.                                                                                                                                                                                                                                                                                                                                                         |
| **name**                  | Benennt die Assembly eindeutig. Verwenden Sie das folgende Format für den Assemblynamen: Organization.Division.Name. Beispiel: Microsoft. Windows.mysampleAsm. Erforderlich. Beachten Sie, dass im Fall einer DLL, die als private Assembly mit einer separaten Manifestdatei gepackt ist, der Name der Assembly vom Namen der DLL und des Manifests abweichen muss.<br/>                                                                              |
| **language**              | Identifiziert die Sprache der Assembly. Optional. Wenn die Assembly sprachspezifisch ist, geben Sie den DHTML-Sprachcode an. Weglassen Sie im DEF-Kontext **assemblyIdentity** eines Assemblymanifests, das für die weltweite Verwendung bestimmt ist (sprachneutral), das Sprachattribut aus.<br/> Legen Sie in einem REF-Kontext **assemblyIdentity** eines Assemblymanifests für die weltweite Verwendung (sprachneutral) den Wert der Sprache auf \* " " fest.<br/> |
| **processorArchitecture** | Gibt den Prozessor an. Die gültigen Werte sind x86 für 32-Bit-Windows und ia64 für 64-Bit-Windows. Optional.                                                                                                                                                                                                                                                                                                                               |
| **version**               | Gibt die Assemblyversion an. Verwenden Sie das vierteilige Versionsformat: mmmmm.nnnnn.ooooo.apkpp. Jeder teil, der durch Zeiträume getrennt ist, kann 0-65535 einschließlich sein. Weitere Informationen finden Sie unter [Assemblyversionen.](assembly-versions.md) Erforderlich.                                                                                                                                                                                               |
| **Publickeytoken**        | Eine Hexadezimalzeichenfolge mit 16 Zeichen, die die letzten 8 Bytes des SHA-1-Hashs des öffentlichen Schlüssels darstellt, unter dem die Assembly signiert ist. Der zum Signieren des Katalogs verwendete öffentliche Schlüssel muss 2048 Bit oder höher sein. Erforderlich für freigegebene nebeneinander verwendete Assemblys.                                                                                                                                                                                |



 

</dd> <dt>

<span id="dependency"></span><span id="DEPENDENCY"></span>**Abhängigkeit**
</dt> <dd>

Ein Containerelement, das mindestens ein **dependentAssembly-Element** enthält. Das erste Unterelement muss ein **dependentAssembly-Element** sein. Eine **Abhängigkeit** weist keine Attribute auf. Optional.

</dd> <dt>

<span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>**Dependentassembly**
</dt> <dd>

Das erste Unterelement muss ein **assemblyIdentity-Element** sein, das eine side-by-side-Assembly beschreibt und eindeutig identifiziert, die von der side-by-side-Assembly verwendet wird, die dieses Assemblymanifest besitzt. Jede **dependentAssembly** muss sich innerhalb genau einer **Abhängigkeit** befinden. Optional.

</dd> <dt>

<span id="file"></span><span id="FILE"></span>**Datei**
</dt> <dd>

Enthält Dateien, die von einer nebeneinander verwendeten Assembly verwendet werden. Enthält **comClass-,** **typelib-, windowClass-,**  **comInterfaceProxyStub-Unterelemente.** Optional.

Das **Dateielement** weist die folgenden Attribute auf.



| attribute   | Beschreibung                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------|
| **name**    | Name der Datei, z. B. Conctl32.dll.                                                            |
| **Hashalg** | Algorithmus, der zum Erstellen eines Hashs der Datei verwendet wird. Dieser Wert sollte SHA1 sein.                                 |
| **hash**    | Ein Hash der Datei, auf die durch den Namen verwiesen wird. Eine hexadezimale Zeichenfolge der Länge, die vom Hashalgorithmus abhängt. |



 

</dd> <dt>

<span id="comClass"></span><span id="comclass"></span><span id="COMCLASS"></span>**comClass**
</dt> <dd>

Ein Unterelement  eines Dateielements. Optional.

Das **comClass-Element** verfügt über die folgenden Attribute.



| attribute               | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **description**         | Klassenname.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Clsid**               | Die GUID, die die Klasse eindeutig identifiziert. Erforderlich. Der Wert muss das Format einer gültigen GUID aufweisen.                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **threadingModel**      | Das threadingmodell, das von prozessübergreifenden COM-Klassen verwendet wird. Wenn diese Eigenschaft NULL ist, wird kein Threadingmodell verwendet. Die Komponente wird im Hauptthread des Clients erstellt, und Aufrufe von anderen Threads werden an diesen Thread gemarshallt. Optional. Gültige Werte sind: "Apartment", "Free", "Both" und "Neutral".                                                                                                                                                                                                                         |
| **tlbid**               | GUID für die Typbibliothek für diese COM-Komponente. Der Wert muss das Format einer GUID aufweisen. Optional.                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **Progid**              | Versionsabhängige programmgesteuerter Bezeichner, der der COM-Komponente zugeordnet ist. Das Format einer ProgID ist <*Hersteller*>.<*Komponente*>.<*Version*>.                                                                                                                                                                                                                                                                                                                                                                      |
| **miscStatus**          | Dupliziert im Assemblymanifest die Informationen, die vom MiscStatus-Registrierungsschlüssel bereitgestellt werden. Wenn werte für die **MiscStatusIcon-,** **miscStatusContent-,** **miscStatusDocprint-** oder **miscStatusThumbnail-Attribute** nicht gefunden werden, wird der entsprechende Standardwert, der in **miscStatus** aufgeführt ist, für die fehlenden Attribute verwendet. Der Wert kann eine durch Kommas getrennte Liste der Attributwerte aus der folgenden Tabelle sein. Sie können dieses Attribut verwenden, wenn die COM-Klasse eine OCX-Klasse ist, die Miscstatus-Registrierungsschlüsselwerte erfordert. |
| **miscStatusIcon**      | Duplikate in der Assembly manifestieren die vom DVASPECT-SYMBOL bereitgestellten \_ Informationen. Sie kann ein Symbol eines Objekts bereitstellen. Der Wert kann eine durch Kommas getrennte Liste der Attributwerte aus der folgenden Tabelle sein. Sie können dieses Attribut verwenden, wenn die COM-Klasse eine OCX-Klasse ist, die Miscstatus-Registrierungsschlüsselwerte erfordert.                                                                                                                                                                                                                |
| **miscStatusContent**   | Duplikate in der Assembly manifestieren die von DVASPECT CONTENT bereitgestellten \_ Informationen. Es kann ein zusammengesetztes Dokument bereitstellen, das für einen Bildschirm oder Drucker angezeigt werden kann. Der Wert kann eine durch Kommas getrennte Liste der Attributwerte aus der folgenden Tabelle sein. Sie können dieses Attribut verwenden, wenn die COM-Klasse eine OCX-Klasse ist, die Miscstatus-Registrierungsschlüsselwerte erfordert.                                                                                                                                                                          |
| **miscStatusDocprint**  | Duplikate in der Assembly manifestieren die von DVASPECT DOCPRINT bereitgestellten \_ Informationen. Sie kann eine Objektdarstellung bereitstellen, die auf dem Bildschirm angezeigt werden kann, als ob sie auf einem Drucker ausgegeben würde. Der Wert kann eine durch Kommas getrennte Liste der Attributwerte aus der folgenden Tabelle sein. Sie können dieses Attribut verwenden, wenn die COM-Klasse eine OCX-Klasse ist, die Miscstatus-Registrierungsschlüsselwerte erfordert.                                                                                                                                               |
| **miscStatusThumbnail** | Duplikate in einer Assembly manifestieren die von DVASPECT THUMBNAIL bereitgestellten \_ Informationen. Sie kann eine Miniaturansicht eines Objekts bereitstellen, das in einem Browsertool angezeigt werden kann. Der Wert kann eine durch Kommas getrennte Liste der Attributwerte aus der folgenden Tabelle sein. Sie können dieses Attribut verwenden, wenn die COM-Klasse eine OCX-Klasse ist, die Miscstatus-Registrierungsschlüsselwerte erfordert.                                                                                                                                                                         |



 

Das **comClass-Element** kann <progid>...</progid> -Elemente als untergeordnete Elemente aufweisen, die die versionsabhängigen Progids auflisten.

Das folgende Beispiel zeigt ein **comClass-Element,** das in einem **Dateielement** enthalten ist.

``` syntax
<file name="sampleu.dll">
        <comClass description="Font Property Page"
    clsid="{0BE35200-8F91-11CE-9DE3-00AA004BB851}"
          threadingModel = "Both"
             tlbid = "{44EC0535-400F-11D0-9DCD-00A0C90391D3}"/>
        <comClass description="Color Property Page"
    clsid="{0BE35201-8F91-11CE-9DE3-00AA004BB851}" 
    progid="ABC.Registrar"/>
    </file>
```

Wenn ihre COM-Klasse eine OCX-Klasse ist, die den MiscStatus-Registrierungsunterschlüssel erfordert, um anzugeben, wie ein Objekt erstellt und angezeigt werden soll, können Sie das Objekt aktivieren, indem Sie diese Informationen im Assemblymanifest duplizieren. Geben Sie die Merkmale des Objekts an, indem Sie die Attribute **miscStatus,** **miscStatusIcon,** **miscStatusContent,** **miscStatusDocprint** und **miscStatusThumbnail** des **comClass-Elements** verwenden. Legen Sie diese Attribute auf eine durch Trennzeichen getrennte Liste von Attributwerten aus der folgenden Tabelle fest. Diese Attribute duplizieren die Informationen, die von einer DVASPECT-Enumeration bereitgestellt werden. Wenn für **miscStatusIcon,** **miscStatusContent,** **miscStatusDocprint** oder **miscStatusThumbnail** kein Wert gefunden wird, werden die in **miscStatus** angegebenen Standardwerte verwendet. Verwenden Sie Attributwerte aus der folgenden Tabelle. Diese entsprechen den Bitflags einer [**OLEMISC-Enumeration.**](/windows/win32/api/oleidl/ne-oleidl-olemisc)



| Attributwert              | OLEMISC-Konstante                      |
|------------------------------|---------------------------------------|
| recomposeonresize            | OLEMISC \_ RECOMPOSEONRESIZE            |
| onlyiconic                   | OLEMISC \_ ONLYICONIC                   |
| insertnotreplace             | OLEMISC \_ INSERTNOTREPLACE             |
| static                       | OLEMISC \_ STATIC                       |
| cantlinkinside               | OLEMISC \_ CANTLINKINSIDE               |
| canlinkbyole1                | OLEMISC \_ CANLINKBYOLE1                |
| islinkobject                 | OLEMISC \_ ISLINKOBJECT                 |
| insideout                    | OLEMISC \_ INSIDEOUT                    |
| activatewhenvisible          | OLEMISC \_ ACTIVATEWHENVISIBLE          |
| renderingisdeviceindependent | OLEMISC \_ RENDERINGISDEVICEINDEPENDENT |
| invisibleatruntime           | OLEMISC \_ INVISIBLEATRUNTIME           |
| alwaysrun                    | OLEMISC \_ ALWAYSRUN                    |
| actslikebutton               | OLEMISC \_ ACTSLIKEBUTTON               |
| actslikelabel                | OLEMISC \_ ACTSLIKELABEL                |
| nouiactivate                 | OLEMISC \_ NOUIACTIVATE                 |
| Justierbar                    | OLEMISC \_ ALIGNABLE                    |
| simpleframe                  | OLEMISC \_ SIMPLEFRAME                  |
| setclientsitefirst           | OLEMISC \_ SETCLIENTSITEFIRST           |
| Imemode                      | TOLEMISC \_ IMEMODE                     |
| ignoreativatewhenvisible     | OLEMISC \_ IGNOREACTIVATEWHENVISIBLE    |
| wantstomenumerge             | OLEMISC \_ WANTSTOMENUMERGE             |
| supportsmultilevelundo       | OLEMISC \_ UNTERSTÜTZTMULTILEVELUNDO       |



 

</dd> <dt>

<span id="typelib"></span><span id="TYPELIB"></span>**Typelib**
</dt> <dd>

Ein Unterelement  eines Dateielements. Optional.

Das **typelib-Element** verfügt über die Attribute, die in der folgenden Tabelle dargestellt sind.



| attribute      | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **tlbid**      | Die eindeutige ID der Typbibliothek. Erforderlich.                                                                                                                                                                                                                                                                                                                                                                                    |
| **version**    | Die zweiteilige Versionsnummer der Typbibliothek. Wenn nur die Nebenversionsnummer zunimmt, werden alle Features der vorherigen Typbibliothek auf kompatible Weise unterstützt. Wenn sich die Hauptversionsnummer ändert, muss Code, der für die Typbibliothek kompiliert wurde, erneut kompiliert werden. Die Versionsnummer der Typbibliothek kann sich von der Versionsnummer der Anwendung unterscheiden. Erforderlich.                                      |
| **helpdir**    | Das Verzeichnis, in dem sich die Hilfedatei für die Typen in der Typbibliothek befindet. Wenn die Anwendung Typbibliotheken für mehrere Sprachen unterstützt, verweisen die Bibliotheken möglicherweise auf verschiedene Dateinamen im Hilfedateiverzeichnis. Wenn kein Wert vorhanden ist, geben Sie "" an. Erforderlich.                                                                                                                                                          |
| **Resourceid** | Die hexadezimale Zeichenfolgendarstellung des Gebietsschemabezeichners (LCID). Es handelt sich um eine bis vier Hexadezimalziffern ohne 0x-Präfix und ohne führende Nullen. Die LCID kann einen neutralen Untersprachenbezeichner aufweisen. Weitere Informationen finden Sie unter [Gebietsschemabezeichner.](/windows/desktop/Intl/locale-identifiers) Optional.                                                                                                                                      |
| **flags**      | Die Zeichenfolgendarstellung der Typbibliotheksflags für diese Typbibliothek. Insbesondere sollte es sich um "RESTRICTED", "CONTROL", "HIDDEN" und "HASDISKIMAGE" handelt. Dies sind die Werte der [**LIBFLAGS-Enumeration**](/windows/win32/api/oaidl/ne-oaidl-libflags) und die gleichen Flags, die im *uLibFlags-Parameter* der [**ICreateTypeLib::SetLibFlags-Methode**](/windows/win32/api/oaidl/nf-oaidl-icreatetypelib-setlibflags) angegeben sind. Optional. |



 

Das folgende Beispiel zeigt ein **typelib-Element,** das in einem **Dateielement** enthalten ist.

``` syntax
<file name="sampleu.dll">
       <typelib tlbid="{44EC0535-400F-11D0-9DCD-00A0C90391D3}"
       version="1.0" helpdir=""/>
</file>
```

</dd> <dt>

<span id="comInterfaceExternalProxyStub"></span><span id="cominterfaceexternalproxystub"></span><span id="COMINTERFACEEXTERNALPROXYSTUB"></span>**comInterfaceExternalProxyStub**
</dt> <dd>

**ComInterfaceExternalProxyStub** ist ein Unterelement eines **Assemblyelements** und wird für Automatisierungsschnittstellen verwendet. Beispiel: [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) und die abgeleiteten Schnittstellen. Optional.

Die Standardmäßige Proxystubimplementierungen sind für die meisten Automatisierungsschnittstellen geeignet, z. B. von [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)abgeleitete Schnittstellen. Der Schnittstellenproxystub und alle anderen externen Proxy-Stub-Schnittstellenimplementierungen müssen in **comInterfaceExternalProxyStub** aufgeführt werden. Das **comInterfaceExternalProxyStub-Element** verfügt über die in der folgenden Tabelle gezeigten Attribute.



| attribute         | Beschreibung                                                                                                                                                                                 |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Iid**           | Die IID der Schnittstelle, für die der Proxy deklariert wird. Erforderlich. Der Wert sollte folgendes Format aufweisen: "{iid}".                                                                         |
| **baseInterface** | Die IID der Schnittstelle, von der das durch das **iid-Attribut beschriebene** abgeleitet wird. Dieses Attribut ist optional. Der Wert sollte folgendes Format aufweisen: "{iid}".                            |
| **numMethods**    | Die Anzahl der von der -Schnittstelle implementierten Methoden. Dieses Attribut ist optional. Der Wert sollte folgendes Format aufweisen: "n".                                                                       |
| **name**          | Name der Schnittstelle, wie er im Code angezeigt wird. Beispiel: "IViewObject". Dies sollte keine beschreibende Zeichenfolge sein. Dieses Attribut ist optional. Der Wert sollte folgendes Format aufweisen: "name". |
| **tlbid**         | Die Typbibliothek, die die Beschreibung der vom **iid-Attribut** angegebenen Schnittstelle enthält. Dieses Attribut ist optional. Der Wert sollte folgendes Format aufweisen: "{tlbid}" .                |
| proxyStubClsid32  | Karten eine IID zu einer CLSID in 32-Bit-Proxy-DLLs.                                                                                                                                                |



 

Das folgende Beispiel zeigt ein **comInterfaceExternalProxyStub-Element.**

``` syntax
<comInterfaceExternalProxyStub 
  name="IAxWinAmbientDispatch" 
    iid="{B6EA2051-048A-11D1-82B9-00C04FB9942E}" 
    numMethods="35" 
  baseInterface="{00000000-0000-0000-C000-000000000046}"/>
```

</dd> <dt>

<span id="comInterfaceProxyStub"></span><span id="cominterfaceproxystub"></span><span id="COMINTERFACEPROXYSTUB"></span>**comInterfaceProxyStub**
</dt> <dd>

Ein Unterelement  eines Dateielements. Optional.

Wenn eine Datei in der Assembly einen Proxystub implementiert, muss das entsprechende Dateitag ein **comInterfaceProxyStub-Unterelement** mit Attributen enthalten, die mit einem **comInterfaceProxyStub-Element** identisch sind. Das Marshallen von Schnittstellen zwischen Prozessen und Threads funktioniert möglicherweise nicht wie erwartet, wenn Sie einige der **comInterfaceProxyStub-Abhängigkeiten** für Ihre Komponente weglassen.

Das **comInterfaceProxyStub-Element** weist die folgenden Attribute auf.



| attribute            | Beschreibung                                                                                                                                                                                                                                                                                                 |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Iid**              | das. IID der Schnittstelle, für die der Proxy deklariert wird. Erforderlich. Der Wert sollte folgendes Format aufweisen: "{iid}".                                                                                                                                                                                        |
| **name**             | Name der Schnittstelle, wie er im Code angezeigt wird. Beispiel: "IViewObject". Dies sollte keine beschreibende Zeichenfolge sein. Dieses Attribut ist optional. Der Wert sollte folgendes Format aufweisen: "name".                                                                                                                 |
| **tlbid**            | Die Typbibliothek, die die Beschreibung der vom **iid-Attribut** angegebenen Schnittstelle enthält. Dieses Attribut ist optional. Der Wert sollte folgendes Format aufweisen: "{tlbid}".                                                                                                                                 |
| **baseInterface**    | Die IID der Schnittstelle, von der das durch das **iid-Attribut beschriebene** abgeleitet wird. Dieses Attribut ist optional. Der Wert sollte folgendes Format aufweisen: "{iid}".                                                                                                                                            |
| **numMethods**       | Die Anzahl der von der -Schnittstelle implementierten Methoden. Dieses Attribut ist optional. Der Wert sollte folgendes Format aufweisen: "n".                                                                                                                                                                                       |
| **proxyStubClsid32** | Karten eine IID zu einer CLSID in 32-Bit-Proxy-DLLs.                                                                                                                                                                                                                                                                |
| **threadingModel**   | Das threadingmodell, das von prozessübergreifenden COM-Klassen verwendet wird. Wenn diese Eigenschaft NULL ist, wird kein Threadingmodell verwendet. Die Komponente wird im Hauptthread des Clients erstellt, und Aufrufe von anderen Threads werden an diesen Thread gemarshallt. Optional. Gültige Werte sind: "Apartment", "Free", "Both" und "Neutral". |



 

</dd> <dt>

<span id="windowclass"></span><span id="WINDOWCLASS"></span>**Windowclass**
</dt> <dd>

Der Name einer Windows-Klasse, die versioniert werden soll. Das **windowclass-Element** weist das folgende Attribut auf.



| attribute     | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Versionierte** | Dieses Attribut steuert, ob der in der Registrierung verwendete interne Fensterklassenname die Version der Assembly enthält, die die Fensterklasse enthält. Der Wert dieses Attributs kann "yes" oder "no" sein. Der Standardwert ist "yes". Der Wert "no" sollte nur verwendet werden, wenn dieselbe Fensterklasse von einer parallelen Komponente und einer entsprechenden nicht parallelen Komponente definiert wird und Sie sie als dieselbe Fensterklasse behandeln möchten. Beachten Sie, dass die üblichen Regeln für die Fensterklassenregistrierung nur die erste Komponente anwenden, die die Fensterklasse registriert, die sie registrieren kann, da sie nicht versioniert ist. |



 

Das folgende Beispiel zeigt ein **windowclass-Element,** das in einem **Dateielement** enthalten ist.

``` syntax
<file name="comctl32.dll">
        <windowClass versioned="no">ToolbarWindow32</windowClass>
</file>
```

</dd> </dl>

## <a name="example"></a>Beispiel

Im Folgenden wird ein Beispiel für ein Assemblymanifest beschrieben.

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" 
manifestVersion="1.0">
    <assemblyIdentity type="win32" name="Microsoft.Tools.SampleAssembly" version="6.0.0.0" processorArchitecture="x86" publicKeyToken="0000000000000000"/>
    <file name="sampleu.dll" hash="3eab067f82504bf271ed38112a4ccdf46094eb5a" hashalg="SHA1">
        <comClass description="Font Property Page" clsid="{0BE35200-8F91-11CE-9DE3-00AA004BB851}"/>
        <comClass description="Color Property Page" clsid="{0BE35201-8F91-11CE-9DE3-00AA004BB851}"/>
        <comClass description="Picture Property Page" clsid="{0BE35202-8F91-11CE-9DE3-00AA004BB851}"/>
    </file>
    <file name="bar.dll" hash="ac72753e5bb20446d88a48c8f0aaae769a962338" hashalg="SHA1"/>
    <file name="foo.dll" hash="a7312a1f6cfb46433001e0540458de60adcd5ec5" hashalg="SHA1">
        <comClass description="Registrar Class" clsid="{44EC053A-400F-11D0-9DCD-00A0C90391D3}" progid="ATL.Registrar"/>
    <comInterfaceProxyStub iid="{B6EA2051-048A-11D1-82B9-00C04FB9942E}" name=" IAxWinAmbientDispatch " tlbid="{34EC053A-400F-11D0-9DCD-00A0C90391D3}"/>
        <typelib tlbid="{44EC0535-400F-11D0-9DCD-00A0C90391D3}" version="1.0" helpdir=""/>
    </file>
    <file name="sampledll.dll" hash="ba62960ceb15073d2598379307aad84f3a73dfcb" hashalg="SHA1"/>
<windowClass>ToolbarWindow32</windowClass>
        <windowClass>ComboBoxEx32</windowClass>
        <windowClass>sample_trackbar32</windowClass>
        <windowClass>sample_updown32</windowClass>
</assembly>
```

 

