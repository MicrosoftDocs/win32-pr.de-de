---
description: Ein Assemblymanifest ist eine XML-Datei, die eine Seite-an-Seite-Assembly beschreibt.
ms.assetid: f7973019-0a80-498e-adf1-c66267c813f4
title: Assembly-Manifeste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 254702d5044331fa5d47def815556dbd8edef2f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216549"
---
# <a name="assembly-manifests"></a>Assembly-Manifeste

Ein Assemblymanifest ist eine XML-Datei, die eine Seite-an-Seite-Assembly beschreibt. Assemblymanifeste beschreiben die Namen und Versionen von parallelen Assemblys, Dateien und Ressourcen der Assembly sowie die Abhängigkeit der Assembly auf anderen parallelen Assemblys. Die korrekte Installation, Aktivierung und Ausführung von parallelen Assemblys erfordert, dass das Assemblymanifest immer einer Assembly im System beiliegt.

Eine umfassende Liste des XML-Schemas finden Sie unter [Manifest-Datei Schema](manifest-file-schema.md).

Assemblymanifeste verfügen über die folgenden Elemente und Attribute.



| Element                           | Attribute                | Erforderlich |
|-----------------------------------|---------------------------|----------|
| **Stadtverordneten**                      |                           | Ja      |
|                                   | **manifestVersion**       | Ja      |
| **nogeerbt werden kann**                 |                           | Nein       |
| **AssemblyIdentity**              |                           | Ja      |
|                                   | **type**                  | Ja      |
|                                   | **name**                  | Ja      |
|                                   | **language**              | Nein       |
|                                   | **processorArchitecture** | Nein       |
|                                   | **version**               | Ja      |
|                                   | **PublicKeyToken**        | Nein       |
| **gkeit**                    |                           | Nein       |
| **dependentAssembly**             |                           | Nein       |
| **datei**                          |                           | Nein       |
|                                   | **name**                  | Ja      |
|                                   | **HashAlg**               | Nein       |
|                                   | **hash**                  | Nein       |
| **ComClass**                      |                           | Nein       |
|                                   | **Beschreibung**           | Nein       |
|                                   | **CLSID**                 | Ja      |
|                                   | **Threading Model**        | Nein       |
|                                   | **tlbid**                 | Nein       |
|                                   | **ProgID**                | Nein       |
|                                   | **fehlstatus**            | Nein       |
|                                   | **falsche Statusmeldung**        | Nein       |
|                                   | **fehlstatus Content**     | Nein       |
|                                   | **fehlstatus docprint**    | Nein       |
|                                   | **fehlstatus docprint**    | Nein       |
| **Export der Typbibliothek**                       |                           | Nein       |
|                                   | **tlbid**                 | Ja      |
|                                   | **version**               | Ja      |
|                                   | **helpDir**               | Ja      |
|                                   | **ResourceId**            | Nein       |
|                                   | **flags**                 | Nein       |
| **comInterfaceExternalProxyStub** |                           | Nein       |
|                                   | **IID**                   | Ja      |
|                                   | **typeinterface wurde**         | Nein       |
|                                   | **NumMethods**            | Nein       |
|                                   | **name**                  | Nein       |
|                                   | **tlbid**                 | Nein       |
|                                   | **proxyStubClsid32**      | Nein       |
| **comInterfaceProxyStub**         |                           | Nein       |
|                                   | **IID**                   | Ja      |
|                                   | **name**                  | Ja      |
|                                   | **tlbid**                 | Nein       |
|                                   | **typeinterface wurde**         | Nein       |
|                                   | **NumMethods**            | Nein       |
|                                   | **proxyStubClsid32**      | Nein       |
|                                   | **Threading Model**        | Nein       |
| **windowClass**                   |                           | Nein       |
|                                   | **Versionsverwaltung**             | Nein       |



 

## <a name="file-location"></a>Dateispeicherort

Assemblymanifeste können an dreispeicher Orten installiert werden:

-   Als Manifeste, die frei [gegebene](/windows/desktop/Msi/shared-assemblies)Assemblys begleiten, sollten Assemblymanifeste als separate Datei im nebeneinander verwendeten Assemblycache installiert werden. Dies ist normalerweise der WinSxS-Ordner im Windows-Verzeichnis.
-   Als Manifeste, die [private](/windows/desktop/Msi/private-assemblies)Assemblys begleiten, sollten Assemblymanifeste in der Verzeichnisstruktur der Anwendung installiert werden. Dabei handelt es sich normalerweise um eine separate Datei im selben Ordner wie die ausführbare Datei der Anwendung.
-   Als Ressource in einer dll ist die Assembly für die private Verwendung der DLL verfügbar. Ein Assemblymanifest kann nicht als Ressource in einer exe-Datei eingeschlossen werden. Eine exe-Datei kann ein [Anwendungs Manifest](application-manifests.md) als Ressource enthalten.

## <a name="file-name-syntax"></a>Dateinamensyntax

Der Name eines Assemblymanifests ist ein beliebiger gültiger Dateiname, gefolgt von. manifest.

Beispielsweise würde ein Assemblymanifest, das auf myAssembly verweist, die folgende Dateiname-Syntax verwenden. Sie können das <Ressourcen- *ID*> Feld weglassen, wenn das Assemblymanifest als separate Datei installiert wird oder wenn die Ressourcen-ID 1 ist.

<dl> myAssembly. <resource ID> . kundiger
</dl>

> [!Note]  
> Aufgrund der Art und Weise, wie eine Seite-an-Seite-Suche nach privaten Assemblys durchzuführen ist, gelten die folgenden Benennungs Einschränkungen beim Verpacken einer DLL als private Assembly Eine empfohlene Vorgehensweise besteht darin, das Assemblymanifest in der dll als Ressource zu platzieren. In diesem Fall muss die Ressourcen-ID gleich 1 und der Name des private Assembly mit dem Namen der dll identisch sein. Wenn beispielsweise der Name der dll Microsoft.Windows.mysample.dll ist, kann der Wert des Namens Attributs, der im **assemblyIdentity** -Element des Manifests verwendet wird, auch Microsoft. Windows. MySample lauten. Eine alternative Möglichkeit besteht darin, das Assemblymanifest in einer separaten Datei zu platzieren. In diesem Fall müssen sich der Name der Assembly und des zugehörigen Manifests von dem Namen der DLL unterscheiden. Beispiel: "Microsoft. Windows. mysampleasm", "Microsoft. Windows. mysampleasm. Manifest" und "Microsoft.Windows.Mysample.dll". Weitere Informationen zur parallelen Suche von privaten Assemblys finden Sie unter [Assemblysuchsequenz](assembly-searching-sequence.md).

 

## <a name="elements"></a>Elemente

Bei Namen von Elementen und Attributen wird die Groß-/Kleinschreibung beachtet. Bei den Werten von Elementen und Attributen wird die Groß-/Kleinschreibung nicht beachtet, außer dem Wert des Type-Attributs.

<dl> <dt>

<span id="assembly"></span><span id="ASSEMBLY"></span>**Stadtverordneten**
</dt> <dd>

Ein Containerelement. Das erste Unterelement muss ein **assemblyIdentity** -oder ein **novererable** -Element sein. Das Assemblymanifest beschreibt die Seite-an-Seite-Assembly, die durch die **assemblyIdentity** identifiziert wird, eindeutig. Erforderlich.

Das Assembly-Element muss sich im Namespace "urn: Schemas-Microsoft-com: ASM. v1" befinden. Untergeordnete Elemente der Assembly müssen sich ebenfalls in diesem Namespace befinden, durch Vererbung oder durch Tagging.

Das **Assembly** -Element weist das folgende Attribut auf.



| Attribut           | BESCHREIBUNG                                           |
|---------------------|-------------------------------------------------------|
| **manifestVersion** | Das **manifestVersion** -Attribut muss auf 1,0 festgelegt werden. |



 

</dd> <dt>

<span id="noInheritable"></span><span id="noinheritable"></span><span id="NOINHERITABLE"></span>**nogeerbt werden kann**
</dt> <dd>

Fügen Sie dieses Element in ein Assemblymanifest ein, um anzugeben, dass die Assembly die [Aktivierungs Kontexte](activation-contexts.md) und deren Objekte verwaltet. Das **novererable** -Element muss ein untergeordnetes Element eines **Assembly** -Elements sein. Das **assemblyIdentity** -Element sollte nach jedem **novererable** -Element stehen. Das **novererable** -Element ist im Assemblymanifest erforderlich, wenn die Assembly von [Anwendungs Manifesten](application-manifests.md) verwendet wird, die das **noerben** -Element enthalten. Ein **novererable** -Element in einem Anwendungs Manifest hat keine Auswirkung. Ein **novererable** -Element weist keine untergeordneten Elemente auf.

</dd> <dt>

<span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>**AssemblyIdentity**
</dt> <dd>

Beschreibt eine parallele Assembly und identifiziert diese eindeutig.

Als erstes **Unterelement eines** **Assemblyelements wird assemblyIdentity** die parallele Assembly, die dieses Assemblymanifest besitzt, beschreibt und eindeutig identifiziert. Dies wird als DEF-Context **assemblyIdentity des Assemblymanifests** bezeichnet.

Als erstes Unterelement eines **dependentAssembly** -Elements beschreibt **assemblyIdentity** eine Seite-an-Seite-Assembly, die vom DEF-Context **assemblyIdentity** verwendet wird, und identifiziert diese eindeutig. Dies wird als ref-Context **assemblyIdentity des Assemblymanifests** bezeichnet. Die DEF-Context-Assembly erfordert, dass die Ref-Context-Assembly ordnungsgemäß funktioniert. Beachten Sie, dass jede ref-Context- **assemblyIdentity** genau mit einer entsprechenden "Def-Context **assemblyIdentity" im eigenen Assemblymanifest** der referenzierten Assembly übereinstimmen muss.

Dieses Element hat keine unter Elemente. Das **assemblyIdentity** -Element verfügt über die folgenden Attribute.



| Attribut                 | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **type**                  | Gibt den Assemblytyp an. Der Wert muss Win32 lauten und in Kleinbuchstaben. Erforderlich.                                                                                                                                                                                                                                                                                                                                                         |
| **name**                  | Benennt die Assembly eindeutig. Verwenden Sie das folgende Format für den Assemblynamen: Organization.Division.Name. Beispiel: Microsoft. Windows. mysampleasm. Erforderlich. Beachten Sie, dass im Fall einer DLL, die als private Assembly mit einer separaten Manifestressource verpackt ist, der Name der Assembly von dem Namen der dll und dem Manifest abweicht.<br/>                                                                              |
| **language**              | Gibt die Sprache der Assembly an. Dies ist optional. Wenn die Assembly sprachspezifisch ist, müssen Sie den Code der DHTML-Sprache angeben. Im DEF-Kontext **assemblyIdentity eines Assemblymanifests** , das für die weltweite Verwendung (Sprachneutral) vorgesehen ist, lassen Sie das Language-Attribut aus.<br/> Legen Sie in einer ref-Context- **Assemblyidentität eines Assemblymanifests** , das für die weltweite Verwendung vorgesehen ist (Sprachneutral), den Wert der Sprache auf " \* " fest.<br/> |
| **processorArchitecture** | Gibt den Prozessor an. Gültige Werte sind x86 für 32-Bit-Windows und ia64 für 64-Bit-Windows. Dies ist optional.                                                                                                                                                                                                                                                                                                                               |
| **version**               | Gibt die Assemblyversion an. Verwenden Sie das vierteilige Versions Format: mmmmm. nnnnn. Ooooo. ppppp. Alle durch Zeiträume getrennten Teile können 0-65535 einschließlich sein. Weitere Informationen finden Sie unter [Assemblyversionen](assembly-versions.md). Erforderlich.                                                                                                                                                                                               |
| **PublicKeyToken**        | Eine hexadezimale Zeichenfolge mit 16 Zeichen, die die letzten 8 Bytes des SHA-1-Hashs des öffentlichen Schlüssels darstellt, unter dem die Assembly signiert ist. Der öffentliche Schlüssel, der zum Signieren des Katalogs verwendet wird, muss 2048 Bit oder größer sein. Für freigegebene parallele Assemblys erforderlich.                                                                                                                                                                                |



 

</dd> <dt>

<span id="dependency"></span><span id="DEPENDENCY"></span>**gkeit**
</dt> <dd>

Ein Containerelement, das mindestens eine **dependentAssembly** enthält. Das erste Unterelement muss ein **dependentAssembly** -Element sein. Eine **Abhängigkeit** hat keine Attribute. Dies ist optional.

</dd> <dt>

<span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>**dependentAssembly**
</dt> <dd>

Das erste Unterelement muss ein assemblyIdentity-Element sein, das eine parallele Assembly beschreibt und eindeutig identifiziert, die von der parallelen Assembly verwendet wird, die dieses **Assemblymanifest** besitzt. Jede **dependentAssembly** muss sich in genau einer **Abhängigkeit** befinden. Dies ist optional.

</dd> <dt>

<span id="file"></span><span id="FILE"></span>**Datei**
</dt> <dd>

Enthält Dateien, die von einer parallelen Assembly verwendet werden. Enthält die unter Elemente **ComClass**, **Export der Typbibliothek**, **WindowClass**, **comInterfaceProxyStub** . Dies ist optional.

Das **File** -Element verfügt über die folgenden Attribute.



| Attribut   | BESCHREIBUNG                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------|
| **name**    | Der Name der Datei, z. b. Conctl32.dll.                                                            |
| **HashAlg** | Der Algorithmus, der zum Erstellen eines Hashwerts der Datei verwendet wird. Dieser Wert muss SHA1 lauten.                                 |
| **hash**    | Ein Hash der Datei, auf die nach Name verwiesen wird. Eine hexadezimale Zeichenfolge der Länge, abhängig vom Hash Algorithmus. |



 

</dd> <dt>

<span id="comClass"></span><span id="comclass"></span><span id="COMCLASS"></span>**ComClass**
</dt> <dd>

Ein Unterelement eines **File** -Elements. Dies ist optional.

Das **ComClass** -Element verfügt über die folgenden Attribute.



| Attribut               | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Beschreibung**         | Klassenname.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **CLSID**               | Die GUID, die die Klasse eindeutig identifiziert. Erforderlich. Der Wert muss das Format einer gültigen GUID aufweisen.                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **Threading Model**      | Das Threading Modell, das von in-Process-COM-Klassen verwendet wird. Wenn diese Eigenschaft NULL ist, wird kein Threading Modell verwendet. Die Komponente wird im Haupt Thread des Clients erstellt, und Aufrufe von anderen Threads werden an diesen Thread gemarshallt. Dies ist optional. Gültige Werte sind: "Apartment", "Free", "both" und "neutral".                                                                                                                                                                                                                         |
| **tlbid**               | GUID für die Typbibliothek für diese COM-Komponente. Der Wert muss das Format einer GUID aufweisen. Dies ist optional.                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **ProgID**              | Versions abhängiger Programm Bezeichner, der der COM-Komponente zugeordnet ist. Das Format einer ProgID ist <*Anbieter*>. <*Component*>. <*Version*>.                                                                                                                                                                                                                                                                                                                                                                      |
| **fehlstatus**          | Duplikate in der Assembly Manifest die Informationen, die vom Registrierungsschlüssel "fehlstatus" bereitgestellt werden. Wenn die Werte für die Attribute " **fehlstatusicon**", " **fehlstatuscontent**", " **fehlstatusdocprint**" oder " **fehlstatusminiatur** " nicht gefunden werden **, wird der** entsprechende Standardwert für die fehlenden Attribute verwendet. Der Wert kann eine durch Trennzeichen getrennte Liste der Attributwerte aus der folgenden Tabelle sein. Sie können dieses Attribut verwenden, wenn die com-Klasse eine OCX-Klasse ist, für die die Registrierungsschlüssel Werte "fehlstatus" erforderlich sind |
| **falsche Statusmeldung**      | Dupliziert im Assemblymanifest die Informationen, die vom DVASPECT-Symbol bereitgestellt werden \_ . Es kann ein Symbol eines Objekts bereitstellen. Der Wert kann eine durch Trennzeichen getrennte Liste der Attributwerte aus der folgenden Tabelle sein. Sie können dieses Attribut verwenden, wenn die com-Klasse eine OCX-Klasse ist, für die die Registrierungsschlüssel Werte "fehlstatus" erforderlich sind                                                                                                                                                                                                                |
| **fehlstatus Content**   | Duplikate in der Assembly Manifest die Informationen, die von DVASPECT-Inhalten bereitgestellt werden \_ . Sie kann ein zusammengesetztes Dokument bereitstellen, das für einen Bildschirm oder Drucker angezeigt wird. Der Wert kann eine durch Trennzeichen getrennte Liste der Attributwerte aus der folgenden Tabelle sein. Sie können dieses Attribut verwenden, wenn die com-Klasse eine OCX-Klasse ist, für die die Registrierungsschlüssel Werte "fehlstatus" erforderlich sind                                                                                                                                                                          |
| **fehlstatus docprint**  | Duplikate in der Assembly manifeden Informationen, die von DVASPECT docprint bereitgestellt werden \_ . Sie kann eine Objektdarstellung bereitstellen, die auf dem Bildschirm angezeigt wird, als ob Sie auf einem Drucker gedruckt wird. Der Wert kann eine durch Trennzeichen getrennte Liste der Attributwerte aus der folgenden Tabelle sein. Sie können dieses Attribut verwenden, wenn die com-Klasse eine OCX-Klasse ist, für die die Registrierungsschlüssel Werte "fehlstatus" erforderlich sind                                                                                                                                               |
| **fehlstatus-Miniaturansicht** | Duplikate in einem Assemblymanifest die von der DVASPECT-Miniaturansicht bereitgestellten Informationen \_ . Es kann eine Miniaturansicht eines Objekts bereitstellen, das in einem Browsertool angezeigt wird. Der Wert kann eine durch Trennzeichen getrennte Liste der Attributwerte aus der folgenden Tabelle sein. Sie können dieses Attribut verwenden, wenn die com-Klasse eine OCX-Klasse ist, für die die Registrierungsschlüssel Werte "fehlstatus" erforderlich sind                                                                                                                                                                         |



 

Das **ComClass** -Element kann über <progid>...</progid> -Elemente als untergeordnete Elemente verfügen, die die Versions abhängigen ProgIDs auflisten.

Das folgende Beispiel zeigt ein **ComClass** -Element, das in einem **File** -Element enthalten ist.

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

Wenn es sich bei der com-Klasse um eine OCX-Klasse handelt, bei der der Registrierungs Unterschlüssel "fehlstatus" angibt, wie ein Objekt erstellt und angezeigt wird, können Sie das Objekt aktivieren, indem Sie diese Informationen im Assemblymanifest duplizieren. Geben Sie die Eigenschaften des Objekts mit den Attributen " **fehlstatus**", " **fehlstatusicon**", " **fehlstatuscontent**", " **fehlstatusdocprint**" und " **fehlstatusminiatur** " des **ComClass** -Elements an. Legen Sie diese Attribute auf eine durch Trennzeichen getrennte Liste mit Attributwerten aus der folgenden Tabelle fest. Diese Attribute duplizieren die Informationen, die von einer DVASPECT-Enumeration bereitgestellt werden. Wenn kein Wert für " **fehlstatusicon**", " **fehlstatuscontent**", " **fehlstatusdocprint**" oder " **fehlstatusminiatur**" gefunden wird, werden die in " **fehlstatus** " angegebenen Standardwerte verwendet. Verwenden Sie Attributwerte aus der folgenden Tabelle. Diese entsprechen den Bitflags einer [**OLEMISC**](/windows/win32/api/oleidl/ne-oleidl-olemisc) -Enumeration.



| Attributwert              | OLEMISC-Konstante                      |
|------------------------------|---------------------------------------|
| recompoabonresize            | OLEMISC \_ recompoabonresize            |
| onlyiconic                   | OLEMISC \_ onlyiconic                   |
| insertnotreplace             | OLEMISC \_ insertnotreplace             |
| static                       | OLEMISC \_ statisch                       |
| kanlinkinside               | OLEMISC- \_ kanlinkinside               |
| canlinkbyole1                | OLEMISC \_ CANLINKBYOLE1                |
| islinkobject                 | OLEMISC \_ islinkobject                 |
| insiout                    | OLEMISC \_ insiout                    |
| activateeinvisible          | OLEMISC \_ activateeinvisible          |
| renderingisdeviceindependent | OLEMISC \_ renderingisdeviceindependent |
| invisibleatruntime           | OLEMISC \_ invisibleatruntime           |
| alwaysrun                    | OLEMISC \_ alwaysrun                    |
| acsilikebutton               | OLEMISC- \_ acsilikebutton               |
| acsilikelabel                | OLEMISC \_ acsilikelabel                |
| Nomen aktivieren                 | OLEMISC \_ nouiaktivierungs                 |
| alignable                    | OLEMISC- \_ alignable                    |
| simpleframe                  | OLEMISC \_ simpleframe                  |
| zuerst SetClientSite           | zuerst OLEMISC \_ SetClientSite           |
| ImeMode                      | tolemisc \_ ImeMode                     |
| ignoreativate. Visible     | OLEMISC \_ ignoreactivateeinvisible    |
| wantstomenumerge             | OLEMISC \_ wantstomenumerge             |
| supportsmultilevelundo       | OLEMISC \_ supportsmultilevelundo       |



 

</dd> <dt>

<span id="typelib"></span><span id="TYPELIB"></span>**Export der Typbibliothek**
</dt> <dd>

Ein Unterelement eines **File** -Elements. Dies ist optional.

Das **Export der Typbibliothek** -Element verfügt über die in der folgenden Tabelle aufgeführten Attribute.



| Attribut      | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **tlbid**      | Die eindeutige ID der Typbibliothek. Erforderlich.                                                                                                                                                                                                                                                                                                                                                                                    |
| **version**    | Die zweiteilige Versionsnummer der Typbibliothek. Wenn nur die neben Versionsnummer zunimmt, werden alle Funktionen der vorherigen Typbibliothek auf kompatible Weise unterstützt. Wenn die Hauptversionsnummer geändert wird, muss der Code, der für die Typbibliothek kompiliert wurde, neu kompiliert werden. Die Versionsnummer der Typbibliothek kann sich von der Versionsnummer der Anwendung unterscheiden. Erforderlich.                                      |
| **helpDir**    | Das Verzeichnis, in dem sich die Hilfedatei für die Typen in der Typbibliothek befindet. Wenn die Anwendung Typbibliotheken für mehrere Sprachen unterstützt, verweisen die Bibliotheken möglicherweise auf unterschiedliche Dateinamen im Hilfe Dateiverzeichnis. Wenn kein Wert angegeben ist, geben Sie "" an. Erforderlich.                                                                                                                                                          |
| **ResourceId** | Die hexadezimale Zeichen folgen Darstellung des Gebiets Schema Bezeichners (Locale Identifier, LCID). Es handelt sich um eine bis vier hexadezimale Ziffern ohne 0x-Präfix und ohne führende Nullen. Die LCID weist möglicherweise einen neutralen unter Sprachen Bezeichner auf. Weitere Informationen finden Sie unter [](/windows/desktop/Intl/locale-identifiers)Gebiets Schema Bezeichner. Dies ist optional.                                                                                                                                      |
| **flags**      | Die Zeichen folgen Darstellung der Typbibliothekflags für diese Typbibliothek. Dabei sollte es sich um einen "eingeschränkten", "Control", "Hidden" und "HASDISKIMAGE" handeln. Dabei handelt es sich um die Werte der [**LIBFLAGS**](/windows/win32/api/oaidl/ne-oaidl-libflags) -Enumeration, und es handelt sich um dieselben Flags, die im Parameter " *ulibflags* " der [**ikreatetypelib:: setlibflags**](/windows/win32/api/oaidl/nf-oaidl-icreatetypelib-setlibflags) -Methode angegeben sind. Dies ist optional. |



 

Das folgende Beispiel zeigt ein **Export der Typbibliothek** -Element, das in einem **File** -Element enthalten ist.

``` syntax
<file name="sampleu.dll">
       <typelib tlbid="{44EC0535-400F-11D0-9DCD-00A0C90391D3}"
       version="1.0" helpdir=""/>
</file>
```

</dd> <dt>

<span id="comInterfaceExternalProxyStub"></span><span id="cominterfaceexternalproxystub"></span><span id="COMINTERFACEEXTERNALPROXYSTUB"></span>**comInterfaceExternalProxyStub**
</dt> <dd>

**ComInterfaceExternalProxyStub** ist ein untergeordnetes **Element eines Assemblyelements und** wird für Automatisierungs Schnittstellen verwendet. Beispielsweise [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) und seine abgeleiteten Schnittstellen. Dies ist optional.

Die Standard Implementierung für proxystubs eignet sich für die meisten Automatisierungs Schnittstellen, wie z. b. von [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)abgeleitete Schnittstellen. Der schnittstellenproxystub und alle anderen externen ProxyStub-Schnittstellen Implementierungen müssen im **comInterfaceExternalProxyStub** aufgeführt werden. Das **comInterfaceExternalProxyStub** -Element verfügt über die in der folgenden Tabelle aufgeführten Attribute.



| Attribut         | BESCHREIBUNG                                                                                                                                                                                 |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **IID**           | Die IID der Schnittstelle, für die der Proxy deklariert wird. Erforderlich. Der Wert muss folgendes Format aufweisen: "{iid}".                                                                         |
| **typeinterface wurde** | Die IID der Schnittstelle, von der das durch das **IID** -Attribut beschriebene Element abgeleitet wird. Dieses Attribut ist optional. Der Wert muss folgendes Format aufweisen: "{iid}".                            |
| **NumMethods**    | Die Anzahl der Methoden, die von der-Schnittstelle implementiert werden. Dieses Attribut ist optional. Der Wert muss folgendes Format aufweisen: "n".                                                                       |
| **name**          | Der Name der Schnittstelle, wie er im Code angezeigt wird. Beispiel: "IViewObject". Dies sollte keine beschreibende Zeichenfolge sein. Dieses Attribut ist optional. Der Wert muss folgendes Format aufweisen: "Name". |
| **tlbid**         | Die Typbibliothek, die die Beschreibung der Schnittstelle enthält, die vom **IID** -Attribut angegeben wird. Dieses Attribut ist optional. Der Wert muss folgendes Format aufweisen: "{TLBID}".                |
| proxyStubClsid32  | Ordnet eine IID einer CLSID in 32-Bit-Proxy-DLLs zu.                                                                                                                                                |



 

Das folgende Beispiel zeigt ein **comInterfaceExternalProxyStub** -Element.

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

Ein Unterelement eines **File** -Elements. Dies ist optional.

Wenn eine Datei in der Assembly einen ProxyStub implementiert, muss das entsprechende Dateitag ein **comInterfaceProxyStub** -Unterelement mit Attributen enthalten, die mit einem **comInterfaceProxyStub** -Element identisch sind. Das Marshalling von Schnittstellen zwischen Prozessen und Threads funktioniert möglicherweise nicht wie erwartet, wenn Sie einige der **comInterfaceProxyStub** -Abhängigkeiten für die Komponente weglassen.

Das **comInterfaceProxyStub** -Element verfügt über die folgenden Attribute.



| Attribut            | BESCHREIBUNG                                                                                                                                                                                                                                                                                                 |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **IID**              | Die. IID der Schnittstelle, für die der Proxy deklariert wird. Erforderlich. Der Wert muss folgendes Format aufweisen: "{iid}".                                                                                                                                                                                        |
| **name**             | Der Name der Schnittstelle, wie er im Code angezeigt wird. Beispiel: "IViewObject". Dies sollte keine beschreibende Zeichenfolge sein. Dieses Attribut ist optional. Der Wert muss folgendes Format aufweisen: "Name".                                                                                                                 |
| **tlbid**            | Die Typbibliothek, die die Beschreibung der Schnittstelle enthält, die vom **IID** -Attribut angegeben wird. Dieses Attribut ist optional. Der Wert muss folgendes Format aufweisen: "{TLBID}".                                                                                                                                 |
| **typeinterface wurde**    | Die IID der Schnittstelle, von der das durch das **IID** -Attribut beschriebene Element abgeleitet wird. Dieses Attribut ist optional. Der Wert muss folgendes Format aufweisen: "{iid}".                                                                                                                                            |
| **NumMethods**       | Die Anzahl der Methoden, die von der-Schnittstelle implementiert werden. Dieses Attribut ist optional. Der Wert muss folgendes Format aufweisen: "n".                                                                                                                                                                                       |
| **proxyStubClsid32** | Ordnet eine IID einer CLSID in 32-Bit-Proxy-DLLs zu.                                                                                                                                                                                                                                                                |
| **Threading Model**   | Das Threading Modell, das von in-Process-COM-Klassen verwendet wird. Wenn diese Eigenschaft NULL ist, wird kein Threading Modell verwendet. Die Komponente wird im Haupt Thread des Clients erstellt, und Aufrufe von anderen Threads werden an diesen Thread gemarshallt. Dies ist optional. Gültige Werte sind: "Apartment", "Free", "both" und "neutral". |



 

</dd> <dt>

<span id="windowclass"></span><span id="WINDOWCLASS"></span>**WindowClass**
</dt> <dd>

Der Name einer Windows-Klasse, die mit Versions Angabe versehen werden soll. Das **WindowClass** -Element weist das folgende Attribut auf.



| Attribut     | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Versionsverwaltung** | Dieses Attribut steuert, ob der in der Registrierung verwendete interne Name der Fenster Klasse die Version der Assembly enthält, die die Fenster Klasse enthält. Der Wert dieses Attributs kann "yes" oder "No" lauten. Der Standardwert ist "yes". Der Wert "No" sollte nur verwendet werden, wenn die gleiche Fenster Klasse durch eine Seite-an-Seite-Komponente und eine äquivalente nicht parallele Komponente definiert ist und Sie diese als dieselbe Fenster Klasse behandeln möchten. Beachten Sie, dass die üblichen Regeln zur Fenster Klassen Registrierung nur die erste Komponente anwenden, mit der die Fenster Klasse registriert wird, da Sie nicht mit Versions Angabe versehen ist. |



 

Das folgende Beispiel zeigt ein **WindowClass** -Element, das in einem **File** -Element enthalten ist.

``` syntax
<file name="comctl32.dll">
        <windowClass versioned="no">ToolbarWindow32</windowClass>
</file>
```

</dd> </dl>

## <a name="example"></a>Beispiel

Im folgenden finden Sie ein Beispiel für ein Assemblymanifest.

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

 

