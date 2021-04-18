---
description: Wenn ein Fehler auftritt, gibt WMI einen Fehlercode als HRESULT-Wert zurück. Diese Codes können von Skripts, C++-Anwendungen oder WMIC zurückgegeben werden.
ms.assetid: b560f37c-da22-4745-8d1f-b27afdf572ec
ms.tgt_platform: multiple
title: WMI-Fehler Konstanten (wbemcli. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e95db7220bdc9669716dbe19f5bf2f4e139dfe5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368211"
---
# <a name="wmi-error-constants"></a>WMI-Fehler Konstanten

Wenn ein Fehler auftritt, gibt WMI einen Fehlercode als **HRESULT** -Wert zurück. Diese Codes können von Skripts, C++-Anwendungen oder [**WMIC**](wmic.md)zurückgegeben werden.

> [!Note]
>
> Die folgende Dokumentation richtet sich an Entwickler und IT-Administratoren. Wenn Sie ein Endbenutzer sind, bei dem eine Fehlermeldung zu WMI aufgetreten ist, sollten Sie [Microsoft-Support](https://support.microsoft.com/) aufrufen und nach dem Fehlercode suchen, der in der Fehlermeldung angezeigt wird. Weitere Informationen zur Behebung von Problemen mit WMI-Skripts und dem WMI-Dienst finden Sie unter [WMI funktioniert nicht!](/previous-versions/tn-archive/ff406382(v=msdn.10)).
>
> Wenn WMI Fehlermeldungen zurückgibt, beachten Sie, dass Sie möglicherweise nicht auf Probleme im WMI-Dienst oder in WMI-Anbietern hinweisen. Fehler können aus anderen Teilen des Betriebssystems stammen und als Fehler über WMI auftreten. Löschen Sie das WMI-Repository unter Umständen nicht als erste Aktion, da das Löschen des Repository zu Beschädigungen des Systems oder der installierten Anwendungen führen kann.
>
> Um weitere Informationen zur Ursache des Problems zu erhalten, können Sie das Befehlszeilen Tool [WMI-Diagnosehilfsprogramm](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) Diagnose herunterladen und ausführen. Mit diesem Tool wird ein Bericht erstellt, der in der Regel die Ursache des Problems isolieren und Anweisungen zur Behebung des Problems bereitstellen kann. Der Bericht hilft Ihnen auch bei der Unterstützung durch den Microsoft-Support. Sie können die WMI-Diagnosehilfsprogramm [hier](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d)herunterladen.

 

Einige Methoden in WMI-Klassen können System-und Netzwerkfehler Codes zurückgeben (z. b. 64). Sie können die Definition dieser Arten von Fehlercodes überprüfen, indem Sie den Befehl **net helpmsg** im Eingabe Aufforderungs Fenster verwenden. Der Befehl **net helpmsg 64** gibt beispielsweise die folgende Meldung zurück: der angegebene Netzwerkname ist nicht mehr verfügbar.

In der folgenden Liste sind einige allgemeine Fehler Bereiche aufgeführt.

<dl> <dt>

<span id="0x80041068_-_0x80041099"></span><span id="0X80041068_-_0X80041099"></span>0x80041068-0x80041099
</dt> <dd>

Fehler, die von WMI selbst stammen.

Fehler bei einem bestimmten WMI-Vorgang.

-   Ein Fehler in der Anforderung, z. b. eine WQL-Abfrage, oder das Konto verfügt nicht über die richtigen Berechtigungen.
-   Ein WMI-Infrastrukturproblem, z. b. eine falsche CIM-oder DCOM-Registrierung.

</dd> <dt>

<span id="0x8007xxxx"></span><span id="0X8007XXXX"></span>0x8007xxxx
</dt> <dd>

Fehler, die im Kernbetriebssystem auftreten. Diese Art von Fehler kann von WMI aufgrund eines externen Fehlers (z. b. DCOM-Sicherheitsfehler) zurückgegeben werden.

</dd> <dt>

<span id="0x80040xxx"></span><span id="0X80040XXX"></span>0x80040xxx
</dt> <dd>

Fehler, die in DCOM ausgelöst werden. Beispielsweise ist die DCOM-Konfiguration für Vorgänge auf einem Remote Computer möglicherweise falsch.

</dd> <dt>

<span id="0x8005xxxx"></span><span id="0X8005XXXX"></span>0x8005xxxx
</dt> <dd>

Fehler aus ADSI (Active Directory-Dienst Schnittstellen) oder LDAP (Lightweight Directory Access Protocol), z. b. ein Active Directory Zugriffsfehler, wenn die WMI-Active Directory Anbieter verwendet werden.

</dd> </dl>

Einige Methoden in WMI-Klassen können System-und Netzwerkfehler Codes zurückgeben (z. b. 64). Sie können die Definition dieser Arten von Fehlercodes überprüfen, indem Sie den Befehl **net helpmsg** im Eingabe Aufforderungs Fenster verwenden. Der Befehl **net helpmsg 64** gibt beispielsweise die folgende Meldung zurück: der angegebene Netzwerkname ist nicht mehr verfügbar. In C++ können Sie [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) und **C: \\ Windows \\ system32 \\ WBEM \\wmiutils.dll** als Nachrichten Modul angeben.

<dl> <dt>

<span id="WBEM_E_FAILED"></span><span id="wbem_e_failed"></span>**WBEM \_ E \_ fehlgeschlagen**
</dt> <dd> <dl> <dt>

2147749889 (0x80041001)
</dt> <dt>



Fehler beim Abrufen.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NOT_FOUND"></span><span id="wbem_e_not_found"></span>**WBEM \_ E \_ nicht \_ gefunden**
</dt> <dd> <dl> <dt>

2147749890 (0x80041002 angezeigt)
</dt> <dt>



Das Objekt wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_ACCESS_DENIED"></span><span id="wbem_e_access_denied"></span>**WBEM \_ E- \_ Zugriff \_ verweigert**
</dt> <dd> <dl> <dt>

2147749891 (0x80041003)
</dt> <dt>



Der aktuelle Benutzer verfügt nicht über die Berechtigung zum Ausführen der Aktion.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_FAILURE"></span><span id="wbem_e_provider_failure"></span>**Fehler beim WBEM \_ E- \_ Anbieter. \_**
</dt> <dd> <dl> <dt>

2147749892 (0x80041004)
</dt> <dt>



Der Anbieter ist zu einem anderen Zeitpunkt als während der Initialisierung fehlgeschlagen.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_TYPE_MISMATCH"></span><span id="wbem_e_type_mismatch"></span>**WBEM \_ E- \_ Typen Konflikt \_**
</dt> <dd> <dl> <dt>

2147749893 (0x80041005)
</dt> <dt>



Es ist ein Typen Konflikt aufgetreten.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_OUT_OF_MEMORY"></span><span id="wbem_e_out_of_memory"></span>**nicht genügend \_ Arbeits \_ \_ Speicher für \_ WBEM E**
</dt> <dd> <dl> <dt>

2147749894 (0x80041006)
</dt> <dt>



Nicht genügend Arbeitsspeicher für den Vorgang.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_CONTEXT"></span><span id="wbem_e_invalid_context"></span>**WBEM \_ E ( \_ ungültiger \_ Kontext)**
</dt> <dd> <dl> <dt>

2147749895 (0x80041007)
</dt> <dt>



Das [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) -Objekt ist ungültig.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_PARAMETER"></span><span id="wbem_e_invalid_parameter"></span>**\_Ungültiger WBEM E- \_ \_ Parameter**
</dt> <dd> <dl> <dt>

2147749896 (0x80041008)
</dt> <dt>



Einer der Parameter für den Aufruf ist nicht korrekt.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NOT_AVAILABLE"></span><span id="wbem_e_not_available"></span>**WBEM \_ E \_ nicht \_ verfügbar**
</dt> <dd> <dl> <dt>

2147749897 (0x80041009)
</dt> <dt>



Die Ressource (in der Regel ein Remote Server) ist zurzeit nicht verfügbar.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CRITICAL_ERROR"></span><span id="wbem_e_critical_error"></span>**kritischer WBEM \_ E- \_ \_ Fehler**
</dt> <dd> <dl> <dt>

2147749898 (0x8004100a)
</dt> <dt>



Interner, kritischer und unerwarteter Fehler. Melden Sie den Fehler an den technischen Support von Microsoft.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_STREAM"></span><span id="wbem_e_invalid_stream"></span>**WBEM \_ E \_ ungültiger \_ Stream**
</dt> <dd> <dl> <dt>

2147749899 (0x8004100b)
</dt> <dt>



Während einer Remotesitzung wurde mindestens ein Netzwerkpaket beschädigt.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NOT_SUPPORTED"></span><span id="wbem_e_not_supported"></span>**WBEM \_ E \_ \_ wird nicht unterstützt.**
</dt> <dd> <dl> <dt>

2147749900 (0x8004100c)
</dt> <dt>



Die Funktion oder der Vorgang wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_SUPERCLASS"></span><span id="wbem_e_invalid_superclass"></span>**WBEM \_ E \_ ungültige \_ Superclass.**
</dt> <dd> <dl> <dt>

2147749901 (0x8004100d)
</dt> <dt>



Die angegebene übergeordnete Klasse ist ungültig.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_NAMESPACE"></span><span id="wbem_e_invalid_namespace"></span>**WBEM \_ E ( \_ ungültiger \_ Namespace)**
</dt> <dd> <dl> <dt>

2147749902 (0x8004100e)
</dt> <dt>



Der angegebene Namespace wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_OBJECT"></span><span id="wbem_e_invalid_object"></span>**ungültiges WBEM- \_ \_ \_ Objekt**
</dt> <dd> <dl> <dt>

2147749903 (0x8004100f)
</dt> <dt>



Die angegebene Instanz ist ungültig.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_CLASS"></span><span id="wbem_e_invalid_class"></span>**\_ungültige WBEM E- \_ \_ Klasse**
</dt> <dd> <dl> <dt>

2147749904 (0x80041010)
</dt> <dt>



Die angegebene Klasse ist ungültig.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_NOT_FOUND"></span><span id="wbem_e_provider_not_found"></span>**der WBEM \_ E- \_ Anbieter wurde \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

2147749905 (0x80041011)
</dt> <dt>



Der Anbieter, auf den im Schema verwiesen wird, verfügt über keine entsprechende Registrierung.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_PROVIDER_REGISTRATION"></span><span id="wbem_e_invalid_provider_registration"></span>**\_ \_ ungültige \_ Anbieter \_ Registrierung für WBEM E**
</dt> <dd> <dl> <dt>

2147749906
</dt> <dt>



Der im Schema referenzierte Anbieter weist eine falsche oder unvollständige Registrierung auf.

Dieser Fehler kann durch eine Vielzahl von Bedingungen verursacht werden, einschließlich der folgenden:

-   Ein fehlender [ \# pragma-Namespace](pragma-namespace.md) Befehl in der Managed Object Format (MOF)-Datei, die zum Registrieren des Anbieters verwendet wird. Der Anbieter kann im falschen WMI-Namespace registriert werden.
-   Fehler beim Abrufen der com-Registrierung.
-   Das Hostingmodell ist ungültig. Weitere Informationen finden Sie unter [Anbieter Hosting und-Sicherheit](provider-hosting-and-security.md).
-   Eine in der Registrierung angegebene Klasse ist ungültig.
-   Fehler beim Erstellen einer Instanz von oder Erben von der [**\_ \_ Win32Provider**](--win32provider.md) -Klasse, um die Anbieter Registrierung in der MOF-Datei zu erstellen.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_LOAD_FAILURE"></span><span id="wbem_e_provider_load_failure"></span>**Fehler beim Laden des WBEM \_ E- \_ Anbieters \_ \_**
</dt> <dd> <dl> <dt>

2147749907 (0x80041013)
</dt> <dt>



COM kann keinen Provider finden, auf den im Schema verwiesen wird.

Dieser Fehler kann durch eine Vielzahl von Bedingungen verursacht werden, einschließlich der folgenden:

-   Der Anbieter verwendet eine WMI-dll, die nicht mit der LIB-Datei identisch ist, die beim Erstellen des Anbieters verwendet wurde.
-   Die Anbieter-DLL oder eine der DLLs, von denen Sie abhängt, ist beschädigt.
-   Der Anbieter konnte [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver)nicht exportieren.
-   Der in-Process-Anbieter wurde nicht mit dem **regsvr32** -Befehl registriert.
-   Der Out-of-Process-Anbieter wurde nicht mit dem Schalter **/RegServer** registriert. Beispielsweise **myprog.exe/RegServer**.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INITIALIZATION_FAILURE"></span><span id="wbem_e_initialization_failure"></span>**WBEM \_ E- \_ Initialisierungs \_ Fehler**
</dt> <dd> <dl> <dt>

2147749908 (0x80041014)
</dt> <dt>



Die Komponente, z. b. ein Anbieter, konnte aus internen Gründen nicht initialisiert werden.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_TRANSPORT_FAILURE"></span><span id="wbem_e_transport_failure"></span>**WBEM \_ E- \_ Transport \_ Fehler**
</dt> <dd> <dl> <dt>

2147749909 (0x80041015)
</dt> <dt>



Netzwerkfehler, der den normalen Betrieb verhindert.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_OPERATION"></span><span id="wbem_e_invalid_operation"></span>**\_Ungültiger WBEM E- \_ \_ Vorgang**
</dt> <dd> <dl> <dt>

2147749910 (0x80041016)
</dt> <dt>



Der angeforderte Vorgang ist ungültig. Dieser Fehler betrifft i. A. ungültige Versuche, Klassen oder Eigenschaften zu löschen.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_QUERY"></span><span id="wbem_e_invalid_query"></span>**\_ungültige WBEM E- \_ \_ Abfrage**
</dt> <dd> <dl> <dt>

2147749911 (0x80041017)
</dt> <dt>



Die Abfrage war nicht syntaktisch gültig.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_QUERY_TYPE"></span><span id="wbem_e_invalid_query_type"></span>**\_Ungültiger WBEM E- \_ \_ Abfragetyp \_**
</dt> <dd> <dl> <dt>

2147749912 (0x80041018)
</dt> <dt>



Die angeforderte Abfragesprache wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_ALREADY_EXISTS"></span><span id="wbem_e_already_exists"></span>**WBEM \_ E ist \_ bereits \_ vorhanden.**
</dt> <dd> <dl> <dt>

2147749913 (0x80041019)
</dt> <dt>



In einem Put-Vorgang wurde das Flag " **wbemchangeflagkreateonly** " angegeben, aber die Instanz ist bereits vorhanden.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_OVERRIDE_NOT_ALLOWED"></span><span id="wbem_e_override_not_allowed"></span>**außer Kraft Setzung von WBEM \_ E \_ \_ nicht \_ zulässig**
</dt> <dd> <dl> <dt>

2147749914 (0x8004101a)
</dt> <dt>



Der Add-Vorgang kann für diesen Qualifizierer nicht durchgeführt werden, da das besitzende Objekt keine über schreibungen zulässt.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROPAGATED_QUALIFIER"></span><span id="wbem_e_propagated_qualifier"></span>**WBEM \_ E \_ - \_ Qualifizierer**
</dt> <dd> <dl> <dt>

2147749915 (0x8004101b)
</dt> <dt>



Der Benutzer hat versucht, einen Qualifizierer zu löschen, der nicht im Besitz Der Qualifizierer wurde von einer übergeordneten Klasse vererbt.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROPAGATED_PROPERTY"></span><span id="wbem_e_propagated_property"></span>**\_propagierte WBEM E- \_ \_ Eigenschaft**
</dt> <dd> <dl> <dt>

2147749916 (0x8004101c)
</dt> <dt>



Der Benutzer hat versucht, eine Eigenschaft zu löschen, deren Besitzer er nicht war. Die Eigenschaft wurde von einer übergeordneten Klasse vererbt.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNEXPECTED"></span><span id="wbem_e_unexpected"></span>**WBEM \_ E \_ unerwartet**
</dt> <dd> <dl> <dt>

2147749917 (0x8004101d)
</dt> <dt>



Der Client hat eine unerwartete und unzulässige Sequenz von Aufrufen vorgenommen, z. b. das Aufrufen von [**EndEnumeration**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-endenumeration) vor dem Aufrufen von [**beginenumeration**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-beginenumeration).


</dt> </dl> </dd> <dt>

<span id="WBEM_E_ILLEGAL_OPERATION"></span><span id="wbem_e_illegal_operation"></span>**Ungültiger WBEM- \_ \_ \_ Vorgang**
</dt> <dd> <dl> <dt>

2147749918 (0x8004101e)
</dt> <dt>



Der Benutzer hat einen ungültigen Vorgang angefordert, z. b. das Abrufen einer Klasse aus einer Instanz.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CANNOT_BE_KEY"></span><span id="wbem_e_cannot_be_key"></span>**WBEM \_ E \_ darf \_ nicht \_ Schlüssel sein.**
</dt> <dd> <dl> <dt>

2147749919 (0x8004101f)
</dt> <dt>



Unzulässiger Versuch, einen Schlüssel Qualifizierer für eine Eigenschaft anzugeben, die kein Schlüssel sein kann. Die Schlüssel sind in der Klassendefinition für ein Objekt angegeben und können nicht für jede Instanz einzeln geändert werden.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INCOMPLETE_CLASS"></span><span id="wbem_e_incomplete_class"></span>**unvollständige WBEM \_ E- \_ \_ Klasse**
</dt> <dd> <dl> <dt>

2147749920 (0x80041020)
</dt> <dt>



Das aktuelle Objekt ist keine gültige Klassendefinition. Entweder ist sie unvollständig, oder Sie wurde nicht bei WMI mithilfe von " [**errbemubject. \_ Put**](swbemobject-put-.md)" registriert.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_SYNTAX"></span><span id="wbem_e_invalid_syntax"></span>**\_ungültige WBEM E- \_ \_ Syntax**
</dt> <dd> <dl> <dt>

2147749921 (0x80041021)
</dt> <dt>



Die Abfrage ist syntaktisch ungültig.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NONDECORATED_OBJECT"></span><span id="wbem_e_nondecorated_object"></span>**nicht ergänzten WBEM- \_ \_ \_ Objekt**
</dt> <dd> <dl> <dt>

2147749922 (0x80041022)
</dt> <dt>



Für die zukünftige Verwendung reserviert.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_READ_ONLY"></span><span id="wbem_e_read_only"></span>**WBEM \_ E schreibgeschützt \_ \_**
</dt> <dd> <dl> <dt>

2147749923 (0x80041023)
</dt> <dt>



Es wurde versucht, eine schreibgeschützte Eigenschaft zu ändern.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_NOT_CAPABLE"></span><span id="wbem_e_provider_not_capable"></span>**WBEM \_ E \_ - \_ Anbieter \_ ist nicht fähig**
</dt> <dd> <dl> <dt>

2147749924 (0x80041024)
</dt> <dt>



Der Anbieter kann den angeforderten Vorgang nicht ausführen. Dies kann eine Abfrage enthalten, die zu komplex ist, eine Instanz abruft, eine Klasse erstellt oder aktualisiert, eine Klasse löscht oder eine Klasse auflistet.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CLASS_HAS_CHILDREN"></span><span id="wbem_e_class_has_children"></span>**WBEM \_ E- \_ Klasse \_ hat \_ untergeordnete Elemente**
</dt> <dd> <dl> <dt>

2147749925 (0x80041025)
</dt> <dt>



Es wurde versucht, eine Änderung vorzunehmen, durch die eine Unterklasse ungültig wird.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CLASS_HAS_INSTANCES"></span><span id="wbem_e_class_has_instances"></span>**WBEM \_ E- \_ Klasse \_ verfügt über \_ Instanzen**
</dt> <dd> <dl> <dt>

2147749926 (0x80041026)
</dt> <dt>



Es wurde versucht, eine Klasse zu löschen oder zu ändern, die Instanzen enthält.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_QUERY_NOT_IMPLEMENTED"></span><span id="wbem_e_query_not_implemented"></span>**WBEM \_ E- \_ Abfrage \_ nicht \_ implementiert**
</dt> <dd> <dl> <dt>

2147749927 (0x80041027)
</dt> <dt>



Für die zukünftige Verwendung reserviert.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_ILLEGAL_NULL"></span><span id="wbem_e_illegal_null"></span>**WBEM \_ E \_ unzulässig \_ null**
</dt> <dd> <dl> <dt>

2147749928 (0x80041028)
</dt> <dt>



Der Wert Nothing/**null** wurde für eine Eigenschaft angegeben, die über einen Wert verfügen muss, z. b. einen, der durch einen [**Schlüssel**](key-qualifier.md), einen [**indizierten**](optional-qualifiers.md)oder einen **nicht- \_ null** -Qualifizierer gekennzeichnet ist.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_QUALIFIER_TYPE"></span><span id="wbem_e_invalid_qualifier_type"></span>**\_Ungültiger WBEM E- \_ \_ Qualifizierertyp \_**
</dt> <dd> <dl> <dt>

2147749929 (0x80041029)
</dt> <dt>



Der Variant-Wert für einen Qualifizierer wurde bereitgestellt, der kein gültiger qualifizierungstyp ist.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_PROPERTY_TYPE"></span><span id="wbem_e_invalid_property_type"></span>**\_Ungültiger WBEM E- \_ \_ \_ Eigenschaftentyp**
</dt> <dd> <dl> <dt>

2147749930 (0x8004102a)
</dt> <dt>



Der für eine Eigenschaft angegebene CIM-Typ ist ungültig.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_VALUE_OUT_OF_RANGE"></span><span id="wbem_e_value_out_of_range"></span>**\_der Wert von WBEM E liegt \_ \_ außerhalb \_ des zulässigen \_ Bereichs.**
</dt> <dd> <dl> <dt>

2147749931 (0x8004102b)
</dt> <dt>



Die Anforderung wurde mit einem Wert außerhalb des gültigen Bereichs erstellt, oder Sie ist mit dem Typ nicht kompatibel.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CANNOT_BE_SINGLETON"></span><span id="wbem_e_cannot_be_singleton"></span>**WBEM \_ E \_ darf \_ kein \_ Singleton sein.**
</dt> <dd> <dl> <dt>

2147749932 (0x8004102c)
</dt> <dt>



Es wurde ein unzulässiger Versuch unternommen, eine Singleton-Klasse zu erstellen, z. b. wenn die Klasse von einer nicht-Singleton-Klasse abgeleitet wird.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_CIM_TYPE"></span><span id="wbem_e_invalid_cim_type"></span>**WBEM \_ E, \_ ungültiger \_ CIM- \_ Typ**
</dt> <dd> <dl> <dt>

2147749933 (0x8004102d)
</dt> <dt>



Der angegebene CIM-Typ ist ungültig.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_METHOD"></span><span id="wbem_e_invalid_method"></span>**\_ungültige WBEM E- \_ \_ Methode**
</dt> <dd> <dl> <dt>

2147749934 (0x8004102e)
</dt> <dt>



Die angeforderte Methode ist nicht verfügbar.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_METHOD_PARAMETERS"></span><span id="wbem_e_invalid_method_parameters"></span>**\_ \_ ungültige \_ Methoden \_ Parameter für WBEM E**
</dt> <dd> <dl> <dt>

2147749935 (0x8004102f)
</dt> <dt>



Die für die Methode angegebenen Parameter sind ungültig.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_SYSTEM_PROPERTY"></span><span id="wbem_e_system_property"></span>**WBEM \_ E- \_ System \_ Eigenschaft**
</dt> <dd> <dl> <dt>

2147749936 (0x80041030)
</dt> <dt>



Es wurde versucht, Qualifizierer für eine Systemeigenschaft abzurufen.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_PROPERTY"></span><span id="wbem_e_invalid_property"></span>**\_ungültige WBEM E- \_ \_ Eigenschaft**
</dt> <dd> <dl> <dt>

2147749937 (0x80041031)
</dt> <dt>



Der Eigenschaftentyp wird nicht erkannt.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CALL_CANCELLED"></span><span id="wbem_e_call_cancelled"></span>**WBEM \_ E- \_ Rückruf \_ abgebrochen**
</dt> <dd> <dl> <dt>

2147749938 (0x80041032)
</dt> <dt>



Der asynchrone Prozess wurde intern oder vom Benutzer abgebrochen. Beachten Sie, dass der Vorgang aufgrund der zeitlichen Steuerung und der Art des asynchronen Vorgangs möglicherweise nicht wirklich abgebrochen wurde.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_SHUTTING_DOWN"></span><span id="wbem_e_shutting_down"></span>**WBEM \_ E \_ wird \_ heruntergefahren**
</dt> <dd> <dl> <dt>

2147749939 (0x80041033)
</dt> <dt>



Der Benutzer hat einen Vorgang angefordert, während WMI gerade heruntergefahren wird.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROPAGATED_METHOD"></span><span id="wbem_e_propagated_method"></span>**\_propagierte WBEM E- \_ \_ Methode**
</dt> <dd> <dl> <dt>

2147749940 (0x80041034)
</dt> <dt>



Es wurde versucht, einen vorhandenen Methodennamen aus einer übergeordneten Klasse wiederzuverwenden, und die Signaturen stimmen nicht ab.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNSUPPORTED_PARAMETER"></span><span id="wbem_e_unsupported_parameter"></span>**\_nicht unterstützter WBEM E- \_ \_ Parameter**
</dt> <dd> <dl> <dt>

2147749941 (0x80041035)
</dt> <dt>



Mindestens ein Parameterwert (z. B. ein Abfragetext) ist zu komplex oder wird nicht unterstützt. Daher wird WMI aufgefordert, den Vorgang mit einfacheren Parametern erneut auszuführen.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_MISSING_PARAMETER_ID"></span><span id="wbem_e_missing_parameter_id"></span>**\_ \_ fehlende \_ Parameter- \_ ID für WBEM E**
</dt> <dd> <dl> <dt>

2147749942 (0x80041036)
</dt> <dt>



Im Methoden aufruffehlte ein Parameter.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_PARAMETER_ID"></span><span id="wbem_e_invalid_parameter_id"></span>**\_ \_ ungültige Parameter- \_ \_ ID für WBEM E**
</dt> <dd> <dl> <dt>

2147749943 (0x80041037)
</dt> <dt>



Der Methoden Parameter weist einen ungültigen [**ID**](standard-wmi-qualifiers.md) -Qualifizierer auf.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NONCONSECUTIVE_PARAMETER_IDS"></span><span id="wbem_e_nonconsecutive_parameter_ids"></span>**\_ \_ nicht aufeinander folgende Parameter- \_ \_ IDs in WBEM E**
</dt> <dd> <dl> <dt>

2147749944 (0x80041038)
</dt> <dt>



Mindestens ein Methoden Parameter hat [**ID**](standard-wmi-qualifiers.md) -Qualifizierer, die nicht in der Reihenfolge sind.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PARAMETER_ID_ON_RETVAL"></span><span id="wbem_e_parameter_id_on_retval"></span>**WBEM \_ E- \_ Parameter- \_ ID \_ in \_ retval**
</dt> <dd> <dl> <dt>

2147749945 (0x80041039)
</dt> <dt>



Der Rückgabewert einer Methode hat einen [**ID**](standard-wmi-qualifiers.md) -Qualifizierer.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_OBJECT_PATH"></span><span id="wbem_e_invalid_object_path"></span>**WBEM \_ E ( \_ ungültiger \_ Objekt \_ Pfad)**
</dt> <dd> <dl> <dt>

2147749946 (0x8004103a)
</dt> <dt>



Der angegebene Objekt Pfad war ungültig.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_OUT_OF_DISK_SPACE"></span><span id="wbem_e_out_of_disk_space"></span>**WBEM \_ E \_ nicht mehr genügend \_ \_ Speicher \_ Platz**
</dt> <dd> <dl> <dt>

2147749947 (0x8004103b)
</dt> <dt>



Nicht genügend Speicherplatz auf dem Datenträger, oder das Limit von 4 GB auf dem WMI-Repository (CIM-Repository) wurde erreicht.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_BUFFER_TOO_SMALL"></span><span id="wbem_e_buffer_too_small"></span>**WBEM \_ E- \_ Puffer \_ zu \_ klein**
</dt> <dd> <dl> <dt>

2147749948 (0x8004103c)
</dt> <dt>



Der angegebene Puffer war zu klein, um alle Objekte im Enumerator aufzunehmen oder eine Zeichen folgen Eigenschaft zu lesen.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNSUPPORTED_PUT_EXTENSION"></span><span id="wbem_e_unsupported_put_extension"></span>**\_ \_ nicht unterstützte put- \_ \_ Erweiterung für WBEM E**
</dt> <dd> <dl> <dt>

2147749949 (0x8004103d)
</dt> <dt>



Der angeforderte Put-Vorgang wird vom Anbieter nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNKNOWN_OBJECT_TYPE"></span><span id="wbem_e_unknown_object_type"></span>**\_ \_ unbekannter \_ Objekttyp WBEM E \_**
</dt> <dd> <dl> <dt>

2147749950 (0x8004103e)
</dt> <dt>



Beim Mars Hallen wurde ein Objekt mit einem falschen Typ oder einer falschen Version gefunden.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNKNOWN_PACKET_TYPE"></span><span id="wbem_e_unknown_packet_type"></span>**\_ \_ unbekannter \_ \_ Pakettyp WBEM E.**
</dt> <dd> <dl> <dt>

2147749951 (0x8004103f)
</dt> <dt>



Beim Mars Hallen wurde ein Paket mit einem falschen Typ oder einer falschen Version gefunden.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_MARSHAL_VERSION_MISMATCH"></span><span id="wbem_e_marshal_version_mismatch"></span>**nicht übereinstimmende WBEM \_ E \_ Marshal- \_ Version \_**
</dt> <dd> <dl> <dt>

2147749952 (0x80041040)
</dt> <dt>



Das Paket weist eine nicht unterstützte Version auf.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_MARSHAL_INVALID_SIGNATURE"></span><span id="wbem_e_marshal_invalid_signature"></span>**WBEM \_ E \_ Mars Hall \_ ungültige \_ Signatur**
</dt> <dd> <dl> <dt>

2147749953 (0x80041041)
</dt> <dt>



Das Paket ist anscheinend beschädigt.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_QUALIFIER"></span><span id="wbem_e_invalid_qualifier"></span>**Ungültiger WBEM- \_ \_ \_ Qualifizierer**
</dt> <dd> <dl> <dt>

2147749954 (0x80041042)
</dt> <dt>



Es wurde versucht, Qualifizierer zu stimmen, wie z. b. das Einfügen \[ \] von Schlüsseln für ein Objekt anstelle einer Eigenschaft.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_DUPLICATE_PARAMETER"></span><span id="wbem_e_invalid_duplicate_parameter"></span>**WBEM \_ E mit \_ ungültigem \_ doppelten \_ Parameter**
</dt> <dd> <dl> <dt>

2147749955 (0x80041043)
</dt> <dt>



Ein doppelter Parameter wurde in einer CIM-Methode deklariert.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_TOO_MUCH_DATA"></span><span id="wbem_e_too_much_data"></span>**WBEM \_ E \_ zu \_ viele \_ Daten**
</dt> <dd> <dl> <dt>

2147749956 (0x80041044)
</dt> <dt>



Für die zukünftige Verwendung reserviert.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_SERVER_TOO_BUSY"></span><span id="wbem_e_server_too_busy"></span>**WBEM \_ E- \_ Server ist \_ \_ ausgelastet.**
</dt> <dd> <dl> <dt>

2147749957 (0x80041045)
</dt> <dt>



Beim Aufrufen von [**iwbemubjectsink:: Hinweis**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) ist ein Fehler aufgetreten. Der Anbieter kann das Ereignis erneut auslösen.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_FLAVOR"></span><span id="wbem_e_invalid_flavor"></span>**WBEM \_ E ist \_ ungültig. \_**
</dt> <dd> <dl> <dt>

2147749958 (0x80041046)
</dt> <dt>



Die angegebene qualifiziererkonfiguration war ungültig.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CIRCULAR_REFERENCE"></span><span id="wbem_e_circular_reference"></span>**WBEM \_ E \_ Zirkel \_ Verweis**
</dt> <dd> <dl> <dt>

2147749959 (0x80041047)
</dt> <dt>



Es wurde versucht, einen Zirkel Verweis (z. b. eine Klasse von sich selbst abzuleiten) zu erstellen.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNSUPPORTED_CLASS_UPDATE"></span><span id="wbem_e_unsupported_class_update"></span>**WBEM \_ E \_ nicht unterstütztes \_ Klassen \_ Update**
</dt> <dd> <dl> <dt>

2147749960 (0x80041048)
</dt> <dt>



Die angegebene Klasse wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CANNOT_CHANGE_KEY_INHERITANCE"></span><span id="wbem_e_cannot_change_key_inheritance"></span>**WBEM \_ E \_ kann \_ die \_ Schlüssel \_ Vererbung nicht ändern**
</dt> <dd> <dl> <dt>

2147749961 (0x80041049)
</dt> <dt>



Es wurde versucht, einen Schlüssel zu ändern, wenn der Schlüssel bereits von Instanzen oder Unterklassen verwendet wird.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CANNOT_CHANGE_INDEX_INHERITANCE"></span><span id="wbem_e_cannot_change_index_inheritance"></span>**WBEM \_ E \_ kann \_ die \_ Index \_ Vererbung nicht ändern**
</dt> <dd> <dl> <dt>

2147749968 (0x80041050)
</dt> <dt>



Es wurde versucht, einen Index zu ändern, wenn bereits Instanzen oder Unterklassen den Index verwenden.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_TOO_MANY_PROPERTIES"></span><span id="wbem_e_too_many_properties"></span>**WBEM \_ E \_ zu \_ viele \_ Eigenschaften**
</dt> <dd> <dl> <dt>

2147749969 (0x80041051)
</dt> <dt>



Es wurde versucht, mehr Eigenschaften zu erstellen, als von der aktuellen Version der Klasse unterstützt werden.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UPDATE_TYPE_MISMATCH"></span><span id="wbem_e_update_type_mismatch"></span>**WBEM \_ E \_ - \_ Updatetyp \_ stimmen nicht überein.**
</dt> <dd> <dl> <dt>

2147749970 (0x80041052)
</dt> <dt>



Die Eigenschaft wurde mit einem in Konflikt stehenden Typ in einer abgeleiteten Klasse neu definiert.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UPDATE_OVERRIDE_NOT_ALLOWED"></span><span id="wbem_e_update_override_not_allowed"></span>**außer Kraft Setzung von WBEM \_ E- \_ Updates \_ \_ nicht \_ zulässig**
</dt> <dd> <dl> <dt>

2147749971 (0x80041053)
</dt> <dt>



Es wurde versucht, in einer abgeleiteten Klasse einen Qualifizierer zu überschreiben, der nicht überschrieben werden kann.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UPDATE_PROPAGATED_METHOD"></span><span id="wbem_e_update_propagated_method"></span>**\_propagierte WBEM E- \_ Update \_ \_ Methode**
</dt> <dd> <dl> <dt>

2147749972 (0x80041054)
</dt> <dt>



Die Methode wurde mit einer in Konflikt stehenden Signatur in einer abgeleiteten Klasse neu deklariert.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_METHOD_NOT_IMPLEMENTED"></span><span id="wbem_e_method_not_implemented"></span>**WBEM \_ E- \_ Methode \_ nicht \_ implementiert**
</dt> <dd> <dl> <dt>

2147749973 (0x80041055)
</dt> <dt>



Es wurde versucht, eine Methode auszuführen, die nicht \[ mit \] in einer relevanten Klasse implementiert ist.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_METHOD_DISABLED"></span><span id="wbem_e_method_disabled"></span>**WBEM \_ E- \_ Methode \_ deaktiviert**
</dt> <dd> <dl> <dt>


</dt> <dt>



Es wurde versucht, eine mit "deaktiviert" markierte Methode auszuführen \[ \] .


</dt> </dl> </dd> <dt>

<span id="WBEM_E_REFRESHER_BUSY"></span><span id="wbem_e_refresher_busy"></span>**WBEM \_ E- \_ Auffrischung \_ ausgelastet**
</dt> <dd> <dl> <dt>

2147749975 (0x80041057)
</dt> <dt>



Das Aktualisierungs Programm ist mit einem anderen Vorgang ausgelastet.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNPARSABLE_QUERY"></span><span id="wbem_e_unparsable_query"></span>**nicht-alisier Bare WBEM- \_ \_ \_ Abfrage**
</dt> <dd> <dl> <dt>

2147749976 (0x80041058)
</dt> <dt>



Die Filter Abfrage ist syntaktisch ungültig.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NOT_EVENT_CLASS"></span><span id="wbem_e_not_event_class"></span>**WBEM \_ E \_ Not ( \_ Ereignis \_ Klasse)**
</dt> <dd> <dl> <dt>

2147749977 (0x80041059)
</dt> <dt>



Die from-Klausel einer Filter Abfrage verweist auf eine Klasse, die keine Ereignisklasse ist (nicht vom [**\_ \_ Ereignis**](--event.md)abgeleitet).


</dt> </dl> </dd> <dt>

<span id="WBEM_E_MISSING_GROUP_WITHIN"></span><span id="wbem_e_missing_group_within"></span>**WBEM \_ E \_ fehlt \_ Gruppe \_ in**
</dt> <dd> <dl> <dt>

2147749978 (0x8004105a)
</dt> <dt>



Eine GROUP BY-Klausel wurde ohne die entsprechende GROUP WITHIN-Klausel verwendet.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_MISSING_AGGREGATION_LIST"></span><span id="wbem_e_missing_aggregation_list"></span>**WBEM \_ E \_ fehlende \_ Aggregations \_ Liste**
</dt> <dd> <dl> <dt>

2147749979 (0x8004105b)
</dt> <dt>



Es wurde eine GROUP BY-Klausel verwendet. Die Aggregation für alle Eigenschaften wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROPERTY_NOT_AN_OBJECT"></span><span id="wbem_e_property_not_an_object"></span>**WBEM \_ E \_ - \_ Eigenschaft \_ kein \_ Objekt**
</dt> <dd> <dl> <dt>

2147749980 (0x8004105c)
</dt> <dt>



Für eine Eigenschaft, die kein eingebettetes Objekt ist, wurde Punktnotation verwendet.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_AGGREGATING_BY_OBJECT"></span><span id="wbem_e_aggregating_by_object"></span>**WBEM \_ E \_ Aggregations \_ nach \_ Objekt**
</dt> <dd> <dl> <dt>

2147749981 (0x8004105d)
</dt> <dt>



Eine GROUP BY-Klausel verweist auf eine Eigenschaft, bei der es sich um ein eingebettetes Objekt ohne Verwendung der Punktnotation handelt.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNINTERPRETABLE_PROVIDER_QUERY"></span><span id="wbem_e_uninterpretable_provider_query"></span>**Abfrage des \_ \_ nicht interpretierbaren WBEM E- \_ Anbieters \_**
</dt> <dd> <dl> <dt>

2147749983 (0x8004105f)
</dt> <dt>



Die Ereignis Anbieter-Registrierungs Abfrage ([**\_ \_ eventproviderregistration**](--eventproviderregistration.md)) hat nicht die Klassen angegeben, für die Ereignisse bereitgestellt wurden.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_BACKUP_RESTORE_WINMGMT_RUNNING"></span><span id="wbem_e_backup_restore_winmgmt_running"></span>**WBEM \_ E \_ Backup \_ Restore \_ WinMgmt wird \_ ausgeführt**
</dt> <dd> <dl> <dt>

2147749984 (0x80041060)
</dt> <dt>



Es wurde angefordert, das Repository zu sichern oder wiederherzustellen, während es von WinMgmt.exe oder vom Svchost-Prozess verwendet wurde, der den WMI-Dienst enthält.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_QUEUE_OVERFLOW"></span><span id="wbem_e_queue_overflow"></span>**Überlauf der WBEM \_ E- \_ Warteschlange \_**
</dt> <dd> <dl> <dt>

2147749985 (0x80041061)
</dt> <dt>



Überlauf der asynchronen Übermittlungs Warteschlange von dem Ereignisconsumer zu langsam.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PRIVILEGE_NOT_HELD"></span><span id="wbem_e_privilege_not_held"></span>**WBEM \_ E- \_ Berechtigung \_ nicht \_ aufrechterhalten**
</dt> <dd> <dl> <dt>

2147749986 (0x80041062)
</dt> <dt>



Der Vorgang konnte nicht ausgeführt werden, da der Client nicht über die erforderlichen Sicherheits Berechtigungen verfügte.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_OPERATOR"></span><span id="wbem_e_invalid_operator"></span>**\_Ungültiger WBEM E- \_ \_ Operator**
</dt> <dd> <dl> <dt>

2147749987 (0x80041063)
</dt> <dt>



Der Operator ist für diesen Eigenschaftentyp ungültig.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_LOCAL_CREDENTIALS"></span><span id="wbem_e_local_credentials"></span>**lokale WBEM \_ E- \_ \_ Anmelde Informationen**
</dt> <dd> <dl> <dt>

2147749988 (0x80041064)
</dt> <dt>



Der Benutzer hat einen Benutzernamen/ein Kennwort/eine Autorität für eine lokale Verbindung angegeben. Der Benutzer muss einen leeren Benutzernamen/ein leeres Kennwort verwenden und auf die Standard Sicherheit zurückgreifen.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CANNOT_BE_ABSTRACT"></span><span id="wbem_e_cannot_be_abstract"></span>**WBEM \_ E \_ darf \_ nicht \_ abstrakt sein.**
</dt> <dd> <dl> <dt>

2147749989 (0x80041065)
</dt> <dt>



Die Klasse wurde als abstrakt erstellt, wenn die übergeordnete Klasse nicht abstrakt ist.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_AMENDED_OBJECT"></span><span id="wbem_e_amended_object"></span>**WBEM \_ E- \_ geändertes \_ Objekt**
</dt> <dd> <dl> <dt>

2147749990 (0x80041066)
</dt> <dt>



Das geänderte Objekt wurde geschrieben, ohne dass das **WBEM- \_ Flag ein \_ \_ geändertes \_ qualifizierungsflag verwendet** .


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CLIENT_TOO_SLOW"></span><span id="wbem_e_client_too_slow"></span>**WBEM \_ E- \_ Client \_ zu \_ langsam**
</dt> <dd> <dl> <dt>

2147749991 (0x80041067)
</dt> <dt>



Der Client hat Objekte nicht schnell genug aus einer Enumeration abgerufen. Diese Konstante wird zurückgegeben, wenn ein Client ein Enumerationsobjekt erstellt, aber nicht rechtzeitig Objekte aus dem Enumerator abruft, was dazu führt, dass die Objekt Caches des Enumerators gesichert werden.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NULL_SECURITY_DESCRIPTOR"></span><span id="wbem_e_null_security_descriptor"></span>**WBEM \_ E \_ NULL- \_ Sicherheits \_ Beschreibung**
</dt> <dd> <dl> <dt>

2147749992 (0x80041068)
</dt> <dt>



NULL-Sicherheits Beschreibung wurde verwendet.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_TIMED_OUT"></span><span id="wbem_e_timed_out"></span>**Timeout bei WBEM \_ E. \_ \_**
</dt> <dd> <dl> <dt>

2147749993 (0x80041069)
</dt> <dt>



Timeout beim Vorgang.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_ASSOCIATION"></span><span id="wbem_e_invalid_association"></span>**WBEM \_ E \_ ungültige Zuordnung \_**
</dt> <dd> <dl> <dt>

2147749994
</dt> <dt>



Die Zuordnung ist ungültig.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_AMBIGUOUS_OPERATION"></span><span id="wbem_e_ambiguous_operation"></span>**mehrdeutiger WBEM- \_ \_ \_ Vorgang**
</dt> <dd> <dl> <dt>

2147749995 (0x8004106b)
</dt> <dt>



Der Vorgang war mehrdeutig.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_QUOTA_VIOLATION"></span><span id="wbem_e_quota_violation"></span>**\_ \_ Kontingent Verletzung für WBEM E \_**
</dt> <dd> <dl> <dt>

2147749996 (0x8004106c)
</dt> <dt>



WMI nimmt zu viel Arbeitsspeicher in Anspruch. Dies kann auf eine geringe Speicherverfügbarkeit oder eine übermäßige Arbeitsspeicher Auslastung durch WMI zurückzuführen sein.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_TRANSACTION_CONFLICT"></span><span id="wbem_e_transaction_conflict"></span>**WBEM \_ E- \_ Transaktions \_ Konflikt**
</dt> <dd> <dl> <dt>

2147749997 (0x8004106d)
</dt> <dt>



Der Vorgang führte zu einem Transaktions Konflikt.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_FORCED_ROLLBACK"></span><span id="wbem_e_forced_rollback"></span>**\_ \_ erzwungenes Rollback für WBEM E \_**
</dt> <dd> <dl> <dt>

2147749998 (0x8004106e)
</dt> <dt>



Die Transaktion hat ein Rollback erzwungen.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNSUPPORTED_LOCALE"></span><span id="wbem_e_unsupported_locale"></span>**von WBEM \_ E \_ nicht unterstütztes Gebiets Schema \_**
</dt> <dd> <dl> <dt>

2147749999 (0x8004106f)
</dt> <dt>



Das im-Befehl verwendete Gebiets Schema wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_HANDLE_OUT_OF_DATE"></span><span id="wbem_e_handle_out_of_date"></span>**WBEM \_ E- \_ handle ist \_ \_ \_ veraltet.**
</dt> <dd> <dl> <dt>

2147750000 (0x80041070)
</dt> <dt>



Objekt Handle ist veraltet.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CONNECTION_FAILED"></span><span id="wbem_e_connection_failed"></span>**WBEM \_ E- \_ Verbindung \_ fehlgeschlagen**
</dt> <dd> <dl> <dt>

2147750001 (0x80041071)
</dt> <dt>



Fehler beim Herstellen einer Verbindung mit der SQL-Datenbank.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_HANDLE_REQUEST"></span><span id="wbem_e_invalid_handle_request"></span>**WBEM \_ E \_ ungültige \_ handle- \_ Anforderung**
</dt> <dd> <dl> <dt>

2147750002 (0x80041072)
</dt> <dt>



Die Handle-Anforderung war ungültig.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROPERTY_NAME_TOO_WIDE"></span><span id="wbem_e_property_name_too_wide"></span>**der \_ Eigenschafts Name für WBEM E ist \_ \_ \_ zu \_ breit.**
</dt> <dd> <dl> <dt>

2147750003 (0x80041073)
</dt> <dt>



Der Eigenschaftsname enthält mehr als 255 Zeichen.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CLASS_NAME_TOO_WIDE"></span><span id="wbem_e_class_name_too_wide"></span>**WBEM \_ E- \_ Klassen \_ Name \_ zu \_ breit**
</dt> <dd> <dl> <dt>

2147750004 (0x80041074)
</dt> <dt>



Der Klassenname enthält mehr als 255 Zeichen.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_METHOD_NAME_TOO_WIDE"></span><span id="wbem_e_method_name_too_wide"></span>**der WBEM \_ E- \_ Methoden \_ Name ist \_ zu \_ breit.**
</dt> <dd> <dl> <dt>

2147750005 (0x80041075)
</dt> <dt>



Der Methodenname enthält mehr als 255 Zeichen.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_QUALIFIER_NAME_TOO_WIDE"></span><span id="wbem_e_qualifier_name_too_wide"></span>**WBEM \_ E \_ - \_ qualifizierername \_ zu \_ breit**
</dt> <dd> <dl> <dt>

2147750006 (0x80041076)
</dt> <dt>



Der qualifizierername enthält mehr als 255 Zeichen.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_RERUN_COMMAND"></span><span id="wbem_e_rerun_command"></span>**Befehl "WBEM \_ E \_ erneut ausführen" \_**
</dt> <dd> <dl> <dt>

2147750007 (0x80041077)
</dt> <dt>



Der SQL-Befehl muss erneut ausgeführt werden, da in SQL ein Deadlock auftritt. Dies kann nur zurückgegeben werden, wenn Daten in einer SQL-Datenbank gespeichert werden.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_DATABASE_VER_MISMATCH"></span><span id="wbem_e_database_ver_mismatch"></span>**WBEM \_ E- \_ Daten Bank Konflikt nicht \_ \_ übereinstimmen**
</dt> <dd> <dl> <dt>

2147750008 (0x80041078)
</dt> <dt>



Die Datenbankversion entspricht nicht der Version, die der Repository-Treiber verarbeitet.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_VETO_DELETE"></span><span id="wbem_e_veto_delete"></span>**WBEM \_ E- \_ Veto \_ Löschen**
</dt> <dd> <dl> <dt>

2147750009 (0x80041079)
</dt> <dt>



Der Löschvorgang kann von WMI nicht ausgeführt werden, da der Anbieter den Löschvorgang nicht zulässt.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_VETO_PUT"></span><span id="wbem_e_veto_put"></span>**WBEM \_ E- \_ Veto \_**
</dt> <dd> <dl> <dt>

2147750010 (0x8004107a)
</dt> <dt>



Der Put-Vorgang kann von WMI nicht ausgeführt werden, da der Anbieter ihn nicht zulässt.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_LOCALE"></span><span id="wbem_e_invalid_locale"></span>**WBEM \_ E, \_ Ungültiges Gebiets Schema \_**
</dt> <dd> <dl> <dt>

2147750016 (0x80041080)
</dt> <dt>



Der angegebene Gebiets Schema Bezeichner für den Vorgang ist ungültig.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_SUSPENDED"></span><span id="wbem_e_provider_suspended"></span>**WBEM \_ E- \_ Anbieter angeh \_ alten**
</dt> <dd> <dl> <dt>

2147750017 (0x80041081)
</dt> <dt>



Der Anbieter wird angehalten.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_SYNCHRONIZATION_REQUIRED"></span><span id="wbem_e_synchronization_required"></span>**WBEM \_ E- \_ Synchronisierung \_ erforderlich**
</dt> <dd> <dl> <dt>

2147750018 (0x80041082)
</dt> <dt>



Das Objekt muss in das WMI-Repository geschrieben und erneut abgerufen werden, bevor der angeforderte Vorgang erfolgreich ausgeführt werden kann. Diese Konstante wird zurückgegeben, wenn ein Objekt committet und abgerufen werden muss, um den Eigenschafts Wert anzuzeigen.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NO_SCHEMA"></span><span id="wbem_e_no_schema"></span>**WBEM \_ E \_ kein \_ Schema**
</dt> <dd> <dl> <dt>

2147750019 (0x80041083)
</dt> <dt>



Der Vorgang kann nicht abgeschlossen werden. Es ist kein Schema verfügbar.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_ALREADY_REGISTERED"></span><span id="wbem_e_provider_already_registered"></span>**der WBEM \_ E- \_ Anbieter wurde \_ bereits \_ registriert.**
</dt> <dd> <dl> <dt>

02147750020 (0x119f D010)
</dt> <dt>



Der Anbieter kann nicht registriert werden, da er bereits registriert ist.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_NOT_REGISTERED"></span><span id="wbem_e_provider_not_registered"></span>**WBEM \_ E- \_ Anbieter \_ nicht \_ registriert**
</dt> <dd> <dl> <dt>

2147750021 (0x80041085)
</dt> <dt>



Der Anbieter wurde nicht registriert.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_FATAL_TRANSPORT_ERROR"></span><span id="wbem_e_fatal_transport_error"></span>**WBEM E schwerwiegender \_ \_ \_ Transport \_ Fehler**
</dt> <dd> <dl> <dt>

2147750022 (0x80041086)
</dt> <dt>



Schwerwiegender Transport Fehler.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_ENCRYPTED_CONNECTION_REQUIRED"></span><span id="wbem_e_encrypted_connection_required"></span>**WBEM \_ E- \_ verschlüsselte \_ Verbindung \_ erforderlich**
</dt> <dd> <dl> <dt>

2147750023 (0x80041087)
</dt> <dt>



Der Benutzer hat versucht, einen Computernamen oder eine Domäne ohne verschlüsselte Verbindung festzulegen.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_TIMED_OUT"></span><span id="wbem_e_provider_timed_out"></span>**Timeout des WBEM \_ E- \_ Anbieters \_ \_**
</dt> <dd> <dl> <dt>

2147750024 (0x80041088)
</dt> <dt>



Ein Anbieter konnte die Ergebnisse innerhalb des angegebenen Timeouts nicht melden.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NO_KEY"></span><span id="wbem_e_no_key"></span>**WBEM \_ E \_ kein \_ Schlüssel**
</dt> <dd> <dl> <dt>

2147750025 (0x80041089)
</dt> <dt>



Der Benutzer hat versucht, eine Instanz ohne definierten Schlüssel zu platzieren.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_DISABLED"></span><span id="wbem_e_provider_disabled"></span>**WBEM \_ E- \_ Anbieter \_ deaktiviert**
</dt> <dd> <dl> <dt>

2147750026 (0x8004108a)
</dt> <dt>



Der Benutzer hat versucht, eine Anbieter Instanz zu registrieren, aber der com-Server für die Anbieter Instanz wurde entladen.


</dt> </dl> </dd> <dt>

<span id="WBEMESS_E_REGISTRATION_TOO_BROAD"></span><span id="wbemess_e_registration_too_broad"></span>**wbechaos \_ E- \_ Registrierung \_ zu \_ breit**
</dt> <dd> <dl> <dt>

2147753985 (0x80042001)
</dt> <dt>



Die Anbieter Registrierung überschneidet sich mit der System Ereignis Domäne.


</dt> </dl> </dd> <dt>

<span id="WBEMESS_E_REGISTRATION_TOO_PRECISE"></span><span id="wbemess_e_registration_too_precise"></span>**wbechaos \_ E \_ \_ zu \_ präzise Registrierung**
</dt> <dd> <dl> <dt>

2147753986 (0x80042002)
</dt> <dt>



In dieser Abfrage wurde keine WITHIN-Klausel verwendet.


</dt> </dl> </dd> <dt>

<span id="WBEMESS_E_AUTHZ_NOT_PRIVILEGED"></span><span id="wbemess_e_authz_not_privileged"></span>**wbechaos \_ E \_ Authz \_ nicht \_ privilegiert**
</dt> <dd> <dl> <dt>

2147753987 (0x80042003)
</dt> <dt>



Dieser Computer verfügt nicht über die erforderlichen Domänen Berechtigungen, um die Sicherheitsfunktionen zu unterstützen, die sich auf die erstellte Abonnement Instanz beziehen. Wenden Sie sich an den Domänen Administrator, um diesen Computer der Windows-Autorisierungs Zugriffs Gruppe hinzuzufügen.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_RETRY_LATER"></span><span id="wbem_e_retry_later"></span>**WBEM \_ E-Wiederholungs \_ Versuch \_ später**
</dt> <dd> <dl> <dt>

2147758081 (0x80043001)
</dt> <dt>



Für die zukünftige Verwendung reserviert.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_RESOURCE_CONTENTION"></span><span id="wbem_e_resource_contention"></span>**WBEM \_ E- \_ Ressourcen Konflikt \_**
</dt> <dd> <dl> <dt>

2147758082 (0x80043002)
</dt> <dt>



Für die zukünftige Verwendung reserviert.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_QUALIFIER_NAME"></span><span id="wbemmof_e_expected_qualifier_name"></span>**wbemmof \_ E \_ - \_ qualifizierername erwartet \_**
</dt> <dd> <dl> <dt>

2147762177 (0x80044001)
</dt> <dt>



Ein qualifizierername wurde erwartet.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_SEMI"></span><span id="wbemmof_e_expected_semi"></span>**wbemmof \_ E \_ erwartet \_ Semi**
</dt> <dd> <dl> <dt>

2147762178 (0x80044002)
</dt> <dt>



Semikolon oder "=" erwartet.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_OPEN_BRACE"></span><span id="wbemmof_e_expected_open_brace"></span>**wbemmof \_ E \_ erwartete \_ öffnende geschweifter \_ Klammer**
</dt> <dd> <dl> <dt>

2147762179 (0x80044003)
</dt> <dt>



Es wurde eine öffnende geschweiften Klammer erwartet.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_CLOSE_BRACE"></span><span id="wbemmof_e_expected_close_brace"></span>**wbemmof \_ E \_ erwartet schließende geschweifter \_ \_ Klammer**
</dt> <dd> <dl> <dt>

2147762180 (0x80044004)
</dt> <dt>



Fehlende schließende geschweifte Klammer oder ein ungültiges Array Element.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_CLOSE_BRACKET"></span><span id="wbemmof_e_expected_close_bracket"></span>**wbemmof \_ E \_ erwartet Schließ \_ Ende \_ Klammer**
</dt> <dd> <dl> <dt>

2147762181 (0x80044005)
</dt> <dt>



Es wurde eine schließende Klammer erwartet.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_CLOSE_PAREN"></span><span id="wbemmof_e_expected_close_paren"></span>**wbemmof \_ E \_ erwartet Schließ \_ Ende \_ Parser**
</dt> <dd> <dl> <dt>

2147762182 (0x80044006)
</dt> <dt>



Schließende Klammer erwartet.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_ILLEGAL_CONSTANT_VALUE"></span><span id="wbemmof_e_illegal_constant_value"></span>**wbemmof \_ E \_ \_ Ungültiger konstanter \_ Wert**
</dt> <dd> <dl> <dt>

2147762183 (0x80044007)
</dt> <dt>



Numerischer Wert außerhalb des gültigen Bereichs oder Zeichen folgen ohne Anführungszeichen.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_TYPE_IDENTIFIER"></span><span id="wbemmof_e_expected_type_identifier"></span>**wbemmof \_ E \_ - \_ \_ Typbezeichner erwartet**
</dt> <dd> <dl> <dt>

2147762184 (0x80044008)
</dt> <dt>



Es wurde ein Typbezeichner erwartet.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_OPEN_PAREN"></span><span id="wbemmof_e_expected_open_paren"></span>**wbemmof \_ E \_ erwartet \_ offene \_ Parser**
</dt> <dd> <dl> <dt>

2147762185 (0x80044009)
</dt> <dt>



Es wurde eine öffnende Klammer erwartet.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_UNRECOGNIZED_TOKEN"></span><span id="wbemmof_e_unrecognized_token"></span>**wbemmof \_ E \_ unbekanntes \_ Token**
</dt> <dd> <dl> <dt>

2147762186 (0x8004400a)
</dt> <dt>



Unerwartetes Token in der Datei.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_UNRECOGNIZED_TYPE"></span><span id="wbemmof_e_unrecognized_type"></span>**wbemmof \_ E \_ unbekannter \_ Typ**
</dt> <dd> <dl> <dt>

2147762187 (0x8004400b)
</dt> <dt>



Unbekannter oder nicht unterstützter Typbezeichner.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_PROPERTY_NAME"></span><span id="wbemmof_e_expected_property_name"></span>**wbemmof \_ E \_ - \_ Eigenschafts \_ Name erwartet**
</dt> <dd> <dl> <dt>

2147762187 (0x8004400b)
</dt> <dt>



Der Eigenschafts-oder Methodenname wurde erwartet.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_TYPEDEF_NOT_SUPPORTED"></span><span id="wbemmof_e_typedef_not_supported"></span>**wbemmof \_ E \_ typedef \_ \_ wird nicht unterstützt.**
</dt> <dd> <dl> <dt>

2147762189 (0x8004400d)
</dt> <dt>



Typedefs und enumerierte Typen werden nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_UNEXPECTED_ALIAS"></span><span id="wbemmof_e_unexpected_alias"></span>**wbemmof \_ E \_ unerwarteter \_ Alias**
</dt> <dd> <dl> <dt>

2147762190 (0x8004400e)
</dt> <dt>



Nur ein Verweis auf ein Klassenobjekt kann einen Alias Wert aufweisen.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_UNEXPECTED_ARRAY_INIT"></span><span id="wbemmof_e_unexpected_array_init"></span>**wbemmof \_ E \_ unerwartete \_ array- \_ Init**
</dt> <dd> <dl> <dt>

2147762191 (0x8004400f)
</dt> <dt>



Unerwartete Array Initialisierung. Arrays müssen mit deklariert werden \[ \] .


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_AMENDMENT_SYNTAX"></span><span id="wbemmof_e_invalid_amendment_syntax"></span>**wbemmof \_ E \_ ungültige \_ Zusatz \_ Syntax**
</dt> <dd> <dl> <dt>

2147762192 (0x80044010)
</dt> <dt>



Die Syntax für den Namespace Pfad ist ungültig.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_DUPLICATE_AMENDMENT"></span><span id="wbemmof_e_invalid_duplicate_amendment"></span>**wbemmof \_ E \_ ungültige \_ doppelte \_ Zusatz Änderung**
</dt> <dd> <dl> <dt>

2147762193 (0x80044011)
</dt> <dt>



Doppelte Konvertierer für die Änderung.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_PRAGMA"></span><span id="wbemmof_e_invalid_pragma"></span>**wbemmof \_ E \_ ungültiges \_ pragma**
</dt> <dd> <dl> <dt>

2147762194 (0x80044012)
</dt> <dt>



auf das [ \# pragma](pragma-namespace.md) muss ein gültiges Schlüsselwort folgen.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_NAMESPACE_SYNTAX"></span><span id="wbemmof_e_invalid_namespace_syntax"></span>**wbemmof \_ E \_ ungültige \_ Namespace \_ Syntax.**
</dt> <dd> <dl> <dt>

2147762195 (0x80044013)
</dt> <dt>



Die Syntax für den Namespace Pfad ist ungültig.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_CLASS_NAME"></span><span id="wbemmof_e_expected_class_name"></span>**wbemmof \_ E \_ erwartet \_ Klassen \_ Name**
</dt> <dd> <dl> <dt>

2147762196 (0x80044014)
</dt> <dt>



Unerwartetes Zeichen im Klassennamen muss ein Bezeichner sein.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_TYPE_MISMATCH"></span><span id="wbemmof_e_type_mismatch"></span>**wbemmof \_ - \_ Typ \_ stimmt nicht überein.**
</dt> <dd> <dl> <dt>

2147762197 (0x80044015)
</dt> <dt>



Der angegebene Wert kann nicht in den entsprechenden Typ gebracht werden.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_ALIAS_NAME"></span><span id="wbemmof_e_expected_alias_name"></span>**wbemmof \_ E \_ \ \_ Alias \_ Name erwartet**
</dt> <dd> <dl> <dt>

2147762198 (0x80044016)
</dt> <dt>



Auf das Dollar Zeichen muss ein Aliasname als Bezeichner folgen.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_CLASS_DECLARATION"></span><span id="wbemmof_e_invalid_class_declaration"></span>**wbemmof \_ E \_ ungültige \_ Klassen \_ Deklaration.**
</dt> <dd> <dl> <dt>

2147762199 (0x80044017)
</dt> <dt>



Die Klassen Deklaration ist ungültig.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_INSTANCE_DECLARATION"></span><span id="wbemmof_e_invalid_instance_declaration"></span>**wbemmof \_ E \_ ungültige \_ \_ Instanzdeklaration.**
</dt> <dd> <dl> <dt>

2147762200 (0x80044018)
</dt> <dt>



Die Instanzdeklaration ist ungültig. Er muss mit "Instanz von" beginnen.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_DOLLAR"></span><span id="wbemmof_e_expected_dollar"></span>**wbemmof \_ E \_ erwartet \_ Dollar**
</dt> <dd> <dl> <dt>

2147762201 (0x80044019)
</dt> <dt>



Erwartetes Dollarzeichen. Ein Alias in der Form "$Name" muss dem "as"-Schlüsselwort folgen.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_CIMTYPE_QUALIFIER"></span><span id="wbemmof_e_cimtype_qualifier"></span>**wbemmof \_ E \_ CimType- \_ Qualifizierer**
</dt> <dd> <dl> <dt>

2147762202 (0x8004401a)
</dt> <dt>



Der Qualifizierer "CimType" kann nicht direkt in einer MOF-Datei angegeben werden. Verwenden Sie die Standardtyp Notation.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_DUPLICATE_PROPERTY"></span><span id="wbemmof_e_duplicate_property"></span>**wbemmof \_ E \_ duplizierte \_ Eigenschaft**
</dt> <dd> <dl> <dt>

2147762203 (0x8004401b)
</dt> <dt>



Es wurde ein doppelter Eigenschaftsname in der MOF-Datei gefunden.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_NAMESPACE_SPECIFICATION"></span><span id="wbemmof_e_invalid_namespace_specification"></span>**wbemmof \_ E \_ ungültige \_ Namespace \_ Spezifikation**
</dt> <dd> <dl> <dt>

2147762204 (0x8004401c)
</dt> <dt>



Die Namespace Syntax ist ungültig. Verweise auf andere Server sind nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_OUT_OF_RANGE"></span><span id="wbemmof_e_out_of_range"></span>**wbemmof \_ E \_ außerhalb \_ des gültigen \_ Bereichs**
</dt> <dd> <dl> <dt>

2147762205 (0x8004401d)
</dt> <dt>



Der Wert liegt außerhalb des zulässigen Bereichs.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_FILE"></span><span id="wbemmof_e_invalid_file"></span>**wbemmof \_ E \_ ungültige \_ Datei.**
</dt> <dd> <dl> <dt>

2147762206 (0x8004401e)
</dt> <dt>



Die Datei ist keine gültige Text-MOF-Datei oder binäre MOF-Datei.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_ALIASES_IN_EMBEDDED"></span><span id="wbemmof_e_aliases_in_embedded"></span>**wbemmof \_ E \_ Aliase \_ in \_ Embedded**
</dt> <dd> <dl> <dt>

2147762207 (0x8004401f)
</dt> <dt>



Eingebettete Objekte können keine Aliase sein.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_NULL_ARRAY_ELEM"></span><span id="wbemmof_e_null_array_elem"></span>**wbemmof \_ E \_ NULL \_ array \_ Elem**
</dt> <dd> <dl> <dt>

2147762208 (0x80044020)
</dt> <dt>



NULL-Elemente in einem Array werden nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_DUPLICATE_QUALIFIER"></span><span id="wbemmof_e_duplicate_qualifier"></span>**wbemmof \_ E- \_ doppelter \_ Qualifizierer**
</dt> <dd> <dl> <dt>

2147762209 (0x80044021)
</dt> <dt>



Der Qualifizierer wurde für das Objekt mehrmals verwendet.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_FLAVOR_TYPE"></span><span id="wbemmof_e_expected_flavor_type"></span>**Typ wbemmof \_ E \_ Erwarteter \_ \_ Typ**
</dt> <dd> <dl> <dt>

2147762210 (0x80044022)
</dt> <dt>



Es wurde ein Typ für die Konfiguration erwartet, z. b. " **starinstance**", " **desubclass**", " **EnableOverride**" oder 


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INCOMPATIBLE_FLAVOR_TYPES"></span><span id="wbemmof_e_incompatible_flavor_types"></span>**wbemmof \_ E \_ inkompatible \_ Geschmacks \_ Typen**
</dt> <dd> <dl> <dt>

2147762211 (0x80044023)
</dt> <dt>



Das Kombinieren von **EnableOverride** und **DisableOverride** für denselben Qualifizierer ist nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_MULTIPLE_ALIASES"></span><span id="wbemmof_e_multiple_aliases"></span>**wbemmof \_ E \_ mehrere \_ Aliase**
</dt> <dd> <dl> <dt>

2147762212 (0x80044024)
</dt> <dt>



Ein Alias kann nicht zweimal verwendet werden.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INCOMPATIBLE_FLAVOR_TYPES2"></span><span id="wbemmof_e_incompatible_flavor_types2"></span>**Wbemmof \_ E \_ nicht \_ kompatibel \_ TYPES2**
</dt> <dd> <dl> <dt>

2147762213 (0x80044025)
</dt> <dt>



Die Kombination von " **restricted**" und " **deinstance** **" oder "** um" ist nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_NO_ARRAYS_RETURNED"></span><span id="wbemmof_e_no_arrays_returned"></span>**wbemmof \_ E \_ keine \_ Arrays \_ zurückgegeben**
</dt> <dd> <dl> <dt>

2147762214 (0x80044026)
</dt> <dt>



Methoden können keine Array Werte zurückgeben.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_MUST_BE_IN_OR_OUT"></span><span id="wbemmof_e_must_be_in_or_out"></span>**wbemmof \_ E \_ muss ein-oder ausgehend \_ sein \_ \_ \_**
</dt> <dd> <dl> <dt>

2147762215 (0x80044027)
</dt> <dt>



Argumente müssen einen **in** -oder **out** -Qualifizierer aufweisen.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_FLAGS_SYNTAX"></span><span id="wbemmof_e_invalid_flags_syntax"></span>**wbemmof \_ E \_ ungültige \_ Flags- \_ Syntax.**
</dt> <dd> <dl> <dt>

2147762216 (0x80044028)
</dt> <dt>



Die Flags-Syntax ist ungültig.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_BRACE_OR_BAD_TYPE"></span><span id="wbemmof_e_expected_brace_or_bad_type"></span>**wbemmof \_ E \_ - \_ Klammer \_ oder \_ \_ fehlerhafter Typ erwartet**
</dt> <dd> <dl> <dt>

2147762217 (0x80044029)
</dt> <dt>



Die abschließende geschweifter Klammer und das Semikolon für eine Klasse fehlen.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_UNSUPPORTED_CIMV22_QUAL_VALUE"></span><span id="wbemmof_e_unsupported_cimv22_qual_value"></span>**Wbemmof \_ E \_ nicht unterstützt \_ CIMV22 \_ Qual- \_ Wert**
</dt> <dd> <dl> <dt>

2147762218 (0x8004402a)
</dt> <dt>



Eine CIM-Version 2,2 wird für einen qualifiziererwert nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_UNSUPPORTED_CIMV22_DATA_TYPE"></span><span id="wbemmof_e_unsupported_cimv22_data_type"></span>**Wbemmof \_ E \_ nicht unterstützter \_ CIMV22- \_ \_ Datentyp**
</dt> <dd> <dl> <dt>

2147762219 (0x8004402b)
</dt> <dt>



Der Datentyp der CIM-Version 2,2 wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_DELETEINSTANCE_SYNTAX"></span><span id="wbemmof_e_invalid_deleteinstance_syntax"></span>**wbemmof \_ E \_ ungültige \_ Delta einstance- \_ Syntax.**
</dt> <dd> <dl> <dt>

2147762220 (0x8004402c)
</dt> <dt>



Die Delete instance-Syntax ist ungültig. Der Wert sollte `#pragma DeleteInstance("instancepath", FAIL|NOFAIL)`


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_QUALIFIER_SYNTAX"></span><span id="wbemmof_e_invalid_qualifier_syntax"></span>**wbemmof \_ E \_ ungültige \_ qualifizierersyntax. \_**
</dt> <dd> <dl> <dt>

2147762221 (0x8004402d)
</dt> <dt>



Die qualifizierersyntax ist ungültig. Dort sollte `qualifiername:type=value,scope(class|instance), flavorname` stehen.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_QUALIFIER_USED_OUTSIDE_SCOPE"></span><span id="wbemmof_e_qualifier_used_outside_scope"></span>**wbemmof \_ E- \_ Qualifizierer außerhalb des Gültigkeits \_ \_ \_ Bereichs**
</dt> <dd> <dl> <dt>

2147762222 (0x8004402e)
</dt> <dt>



Der Qualifizierer wird außerhalb seines Gültigkeits Bereichs verwendet.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_ERROR_CREATING_TEMP_FILE"></span><span id="wbemmof_e_error_creating_temp_file"></span>**wbemmof \_ E \_ Fehler beim Erstellen der temporären \_ \_ \_ Datei.**
</dt> <dd> <dl> <dt>

2147762223 (0x8004402f)
</dt> <dt>



Fehler beim Erstellen der temporären Datei. Die temporäre Datei ist eine Zwischenphase in der MOF-Kompilierung.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_ERROR_INVALID_INCLUDE_FILE"></span><span id="wbemmof_e_error_invalid_include_file"></span>**wbemmof \_ E- \_ Fehler \_ ungültige \_ Includedatei \_**
</dt> <dd> <dl> <dt>

2147762224 (0x80044030)
</dt> <dt>



Eine in der MOF-Datei mit dem Präprozessorbefehl enthaltene Datei ist nicht gültig. [ \# ](-include.md)


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_DELETECLASS_SYNTAX"></span><span id="wbemmof_e_invalid_deleteclass_syntax"></span>**wbemmof \_ E \_ ungültige \_ deleteclass- \_ Syntax.**
</dt> <dd> <dl> <dt>

2147762225 (0x80044031)
</dt> <dt>



Die Syntax für die Präprozessorbefehle ' [ \# pragma DeleteInstance](pragma-deleteinstance.md) ' oder ' [ \# pragma deleteclass](pragma-deleteclass.md) ' ist ungültig.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Header<br/>                   | <dl> <dt>Wbemcli. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Wbemcli. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[WMI-Rückgabe Codes](wmi-return-codes.md)
</dt> </dl>

 

