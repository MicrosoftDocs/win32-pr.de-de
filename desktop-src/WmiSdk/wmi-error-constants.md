---
description: Wenn ein Fehler auftritt, gibt WMI einen Fehlercode als HRESULT-Wert zurück. Diese Codes können von Skripts, C++-Anwendungen oder Wmic zurückgegeben werden.
ms.assetid: b560f37c-da22-4745-8d1f-b27afdf572ec
ms.tgt_platform: multiple
title: WMI-Fehlerkonst constants (WbemCli.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 679fd0cb9714e2ee202b12195b10e72778564d7549ed4731d905603a11e073db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794310"
---
# <a name="wmi-error-constants"></a>WMI-Fehlerkonst constants

Wenn ein Fehler auftritt, gibt WMI einen Fehlercode als **HRESULT-Wert** zurück. Diese Codes können von Skripts, C++-Anwendungen oder [**Wmic zurückgegeben werden.**](wmic.md)

> [!Note]
>
> Die folgende Dokumentation richtet sich an Entwickler und IT-Administratoren. Wenn Sie ein Endbenutzer sind, bei dem eine Fehlermeldung zu WMI aufgetreten ist, sollten Sie zu [Microsoft-Support](https://support.microsoft.com/) wechseln und nach dem Fehlercode suchen, der in der Fehlermeldung angezeigt wird. Weitere Informationen zur Behandlung von Problemen mit WMI-Skripts und dem WMI-Dienst finden Sie unter [WMI Isn't Working!](/previous-versions/tn-archive/ff406382(v=msdn.10)).
>
> Wenn WMI Fehlermeldungen zurückgibt, beachten Sie, dass sie möglicherweise nicht auf Probleme im WMI-Dienst oder in WMI-Anbietern hinweisen. Fehler können aus anderen Teilen des Betriebssystems stammen und über WMI als Fehler auftreten. Löschen Sie das WMI-Repository unter keinen Umständen als erste Aktion, da das Löschen des Repositorys schäden am System oder an installierten Anwendungen verursachen kann.
>
> Um weitere Informationen zur Ursache des Problems zu erhalten, können Sie das WMI-Diagnosehilfsprogramm-Befehlszeilentool herunterladen und ausführen. [](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) Dieses Tool erstellt einen Bericht, der normalerweise die Ursache des Problems isolieren und Anweisungen zum Beheben des Problems bereitstellen kann. Der Bericht unterstützt Auch Microsoft-Supportdienste bei der Unterstützung. Sie können die Datei hier WMI-Diagnosehilfsprogramm [herunterladen.](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d)

 

Einige Methoden in WMI-Klassen können System- und Netzwerkfehlercodes zurückgeben (z. B. 64). Sie können die Definition dieser Arten von Fehlercodes überprüfen, indem Sie den **Befehl net helpmsg** im Eingabeaufforderungsfenster verwenden. Beispielsweise gibt der Befehl **net helpmsg 64** die Folgendes zurück: Der angegebene Netzwerkname ist nicht mehr verfügbar.

In der folgenden Liste sind einige häufige Fehlerbereiche aufgeführt.

<dl> <dt>

<span id="0x80041068_-_0x80041099"></span><span id="0X80041068_-_0X80041099"></span>0x80041068 – 0x80041099
</dt> <dd>

Fehler, die aus WMI selbst stammen.

Fehler bei einem bestimmten WMI-Vorgang aufgrund von

-   Ein Fehler in der Anforderung, z. B. wenn eine WQL-Abfrage fehlschlägt oder das Konto nicht über die richtigen Berechtigungen verfügt.
-   Ein WMI-Infrastrukturproblem, z. B. eine falsche CIM- oder DCOM-Registrierung.

</dd> <dt>

<span id="0x8007xxxx"></span><span id="0X8007XXXX"></span>0x8007xxxx
</dt> <dd>

Fehler, die vom Kernbetriebssystem stammen. WMI gibt diese Art von Fehler möglicherweise aufgrund eines externen Fehlers zurück, z. B. eines DCOM-Sicherheitsfehlers.

</dd> <dt>

<span id="0x80040xxx"></span><span id="0X80040XXX"></span>0x80040xxx
</dt> <dd>

Fehler, die in DCOM auftreten. Beispielsweise kann die DCOM-Konfiguration für Vorgänge auf einem Remotecomputer falsch sein.

</dd> <dt>

<span id="0x8005xxxx"></span><span id="0X8005XXXX"></span>0x8005xxxx
</dt> <dd>

Fehler, der von ADSI (Active Directory-Dienstschnittstellen) oder LDAP (Lightweight Directory Access Protocol) stammt, z. B. ein Active Directory-Zugriffsfehler bei Verwendung der WMI-Active Directory-Anbieter.

</dd> </dl>

Einige Methoden in WMI-Klassen können System- und Netzwerkfehlercodes zurückgeben (z. B. 64). Sie können die Definition dieser Arten von Fehlercodes überprüfen, indem Sie den **Befehl net helpmsg** im Eingabeaufforderungsfenster verwenden. Beispielsweise gibt der Befehl **net helpmsg 64** die Folgendes zurück: Der angegebene Netzwerkname ist nicht mehr verfügbar. In C++ können Sie [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) aufrufen und **C: \\ Windows \\ System32 \\ wbem \\** wmiutils.dllals Nachrichtenmodul angeben.

<dl> <dt>

<span id="WBEM_E_FAILED"></span><span id="wbem_e_failed"></span>**FEHLER bei WBEM \_ E \_**
</dt> <dd> <dl> <dt>

2147749889 (0x80041001)
</dt> <dt>



Fehler beim Aufruf.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NOT_FOUND"></span><span id="wbem_e_not_found"></span>**WBEM \_ E \_ NOT \_ FOUND**
</dt> <dd> <dl> <dt>

2147749890 (0x80041002)
</dt> <dt>



Das Objekt wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_ACCESS_DENIED"></span><span id="wbem_e_access_denied"></span>**WBEM \_ E \_ ACCESS \_ DENIED**
</dt> <dd> <dl> <dt>

2147749891 (0x80041003)
</dt> <dt>



Der aktuelle Benutzer verfügt nicht über die Berechtigung zum Ausführen der Aktion.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_FAILURE"></span><span id="wbem_e_provider_failure"></span>**WBEM E PROVIDER FAILURE (FEHLER BEIM \_ WBEM-E-ANBIETER) \_ \_**
</dt> <dd> <dl> <dt>

2147749892 (0x80041004)
</dt> <dt>



Der Anbieter ist zu einem anderen Zeitpunkt als während der Initialisierung fehlgeschlagen.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_TYPE_MISMATCH"></span><span id="wbem_e_type_mismatch"></span>**WBEM \_ E \_ TYPE \_ MISMATCH**
</dt> <dd> <dl> <dt>

2147749893 (0x80041005)
</dt> <dt>



Typkonflikt.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_OUT_OF_MEMORY"></span><span id="wbem_e_out_of_memory"></span>**WBEM \_ E NICHT GENÜGEND \_ \_ \_ ARBEITSSPEICHER**
</dt> <dd> <dl> <dt>

2147749894 (0x80041006)
</dt> <dt>



Nicht genügend Arbeitsspeicher für den Vorgang.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_CONTEXT"></span><span id="wbem_e_invalid_context"></span>**WBEM \_ E \_ INVALID \_ CONTEXT**
</dt> <dd> <dl> <dt>

2147749895 (0x80041007)
</dt> <dt>



Das [**IWbemContext-Objekt**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) ist ungültig.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_PARAMETER"></span><span id="wbem_e_invalid_parameter"></span>**WBEM \_ E \_ INVALID \_ PARAMETER**
</dt> <dd> <dl> <dt>

2147749896 (0x80041008)
</dt> <dt>



Einer der Parameter für den Aufruf ist nicht korrekt.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NOT_AVAILABLE"></span><span id="wbem_e_not_available"></span>**WBEM \_ E \_ NICHT \_ VERFÜGBAR**
</dt> <dd> <dl> <dt>

2147749897 (0x80041009)
</dt> <dt>



Die Ressource , in der Regel ein Remoteserver, ist derzeit nicht verfügbar.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CRITICAL_ERROR"></span><span id="wbem_e_critical_error"></span>**WBEM \_ E \_ CRITICAL \_ ERROR**
</dt> <dd> <dl> <dt>

2147749898 (0x8004100A)
</dt> <dt>



Interner, kritischer und unerwarteter Fehler. Melden Sie den Fehler an den technischen Support von Microsoft.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_STREAM"></span><span id="wbem_e_invalid_stream"></span>**WBEM \_ E \_ INVALID \_ STREAM**
</dt> <dd> <dl> <dt>

2147749899 (0x8004100B)
</dt> <dt>



Während einer Remotesitzung wurde mindestens ein Netzwerkpaket beschädigt.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NOT_SUPPORTED"></span><span id="wbem_e_not_supported"></span>**WBEM \_ E WIRD NICHT \_ \_ UNTERSTÜTZT**
</dt> <dd> <dl> <dt>

2147749900 (0x8004100C)
</dt> <dt>



Das Feature oder der Vorgang wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_SUPERCLASS"></span><span id="wbem_e_invalid_superclass"></span>**WBEM \_ E \_ INVALID \_ SUPERCLASS**
</dt> <dd> <dl> <dt>

2147749901 (0x8004100D)
</dt> <dt>



Die angegebene übergeordnete Klasse ist ungültig.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_NAMESPACE"></span><span id="wbem_e_invalid_namespace"></span>**WBEM \_ E \_ UNGÜLTIGER \_ NAMESPACE**
</dt> <dd> <dl> <dt>

2147749902 (0x8004100E)
</dt> <dt>



Der angegebene Namespace wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_OBJECT"></span><span id="wbem_e_invalid_object"></span>**WBEM \_ E \_ INVALID \_ OBJECT**
</dt> <dd> <dl> <dt>

2147749903 (0x8004100F)
</dt> <dt>



Die angegebene Instanz ist ungültig.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_CLASS"></span><span id="wbem_e_invalid_class"></span>**WBEM \_ E \_ \_ INVALID-KLASSE**
</dt> <dd> <dl> <dt>

2147749904 (0x80041010)
</dt> <dt>



Die angegebene Klasse ist ungültig.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_NOT_FOUND"></span><span id="wbem_e_provider_not_found"></span>**WBEM E PROVIDER NOT FOUND (WBEM \_ \_ \_ E-ANBIETER NICHT \_ GEFUNDEN)**
</dt> <dd> <dl> <dt>

2147749905 (0x80041011)
</dt> <dt>



Der Anbieter, auf den im Schema verwiesen wird, verfügt nicht über eine entsprechende Registrierung.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_PROVIDER_REGISTRATION"></span><span id="wbem_e_invalid_provider_registration"></span>**WBEM \_ E \_ INVALID \_ PROVIDER \_ REGISTRATION**
</dt> <dd> <dl> <dt>

2147749906
</dt> <dt>



Der Anbieter, auf den im Schema verwiesen wird, verfügt über eine falsche oder unvollständige Registrierung.

Dieser Fehler kann durch viele Bedingungen verursacht werden, einschließlich der folgenden:

-   Ein [ \# fehlender Pragmanamespace-Befehl](pragma-namespace.md) in der Managed Object Format (MOF)-Datei, die zum Registrieren des Anbieters verwendet wird. Der Anbieter kann im falschen WMI-Namespace registriert sein.
-   Fehler beim Abrufen der COM-Registrierung.
-   Das Hostingmodell ist ungültig. Weitere Informationen finden Sie unter [Anbieterhosting und Sicherheit.](provider-hosting-and-security.md)
-   Eine in der Registrierung angegebene Klasse ist ungültig.
-   Fehler beim Erstellen einer Instanz von oder Erben von der [**\_ \_ Win32Provider-Klasse,**](--win32provider.md) um die Anbieterregistrierung in der MOF-Datei zu erstellen.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_LOAD_FAILURE"></span><span id="wbem_e_provider_load_failure"></span>**WBEM \_ E \_ PROVIDER \_ LOAD \_ FAILURE**
</dt> <dd> <dl> <dt>

2147749907 (0x80041013)
</dt> <dt>



COM kann keinen Provider finden, auf den im Schema verwiesen wird.

Dieser Fehler kann durch viele Bedingungen verursacht werden, einschließlich der folgenden:

-   Der Anbieter verwendet eine WMI-DLL, die nicht mit der LIB-Datei überein passt, die beim Erstellen des Anbieters verwendet wurde.
-   Die DLL des Anbieters oder eine der DLLs, von denen sie abhängt, ist beschädigt.
-   Der Anbieter konnte [**dllRegisterServer nicht exportieren.**](/windows/win32/api/olectl/nf-olectl-dllregisterserver)
-   Der In-Process-Anbieter wurde nicht mit dem **Befehl regsvr32** registriert.
-   Der Out-of-Process-Anbieter wurde nicht mit dem **Schalter /regserver** registriert. Beispiel: **myprog.exe /regserver**.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INITIALIZATION_FAILURE"></span><span id="wbem_e_initialization_failure"></span>**FEHLER BEI DER \_ WBEM-E-INITIALISIERUNG \_ \_**
</dt> <dd> <dl> <dt>

2147749908 (0x80041014)
</dt> <dt>



Komponente, z. B. ein Anbieter, konnte aus internen Gründen nicht initialisiert werden.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_TRANSPORT_FAILURE"></span><span id="wbem_e_transport_failure"></span>**WBEM \_ \_ E-TRANSPORTFEHLER \_**
</dt> <dd> <dl> <dt>

2147749909 (0x80041015)
</dt> <dt>



Netzwerkfehler, der den normalen Betrieb verhindert, ist aufgetreten.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_OPERATION"></span><span id="wbem_e_invalid_operation"></span>**WBEM \_ E \_ UNGÜLTIGER \_ VORGANG**
</dt> <dd> <dl> <dt>

2147749910 (0x80041016)
</dt> <dt>



Der angeforderte Vorgang ist ungültig. Dieser Fehler betrifft i. A. ungültige Versuche, Klassen oder Eigenschaften zu löschen.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_QUERY"></span><span id="wbem_e_invalid_query"></span>**WBEM \_ E \_ INVALID \_ QUERY**
</dt> <dd> <dl> <dt>

2147749911 (0x80041017)
</dt> <dt>



Die Abfrage war syntaktisch ungültig.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_QUERY_TYPE"></span><span id="wbem_e_invalid_query_type"></span>**WBEM \_ E \_ UNGÜLTIGER \_ \_ ABFRAGETYP**
</dt> <dd> <dl> <dt>

2147749912 (0x80041018)
</dt> <dt>



Die angeforderte Abfragesprache wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_ALREADY_EXISTS"></span><span id="wbem_e_already_exists"></span>**WBEM \_ E IST BEREITS \_ \_ VORHANDEN**
</dt> <dd> <dl> <dt>

2147749913 (0x80041019)
</dt> <dt>



In einem put-Vorgang wurde das **Flag wbemChangeFlagCreateOnly** angegeben, aber die Instanz ist bereits vorhanden.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_OVERRIDE_NOT_ALLOWED"></span><span id="wbem_e_override_not_allowed"></span>**WBEM \_ \_ E-AUßERKRAFTSETZUNG \_ NICHT \_ ZULÄSSIG**
</dt> <dd> <dl> <dt>

2147749914 (0x8004101A)
</dt> <dt>



Es ist nicht möglich, den Add-Vorgang für diesen Qualifizierer durchzuführen, da das besitzende Objekt keine Überschreibungen zulasst.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROPAGATED_QUALIFIER"></span><span id="wbem_e_propagated_qualifier"></span>**WBEM \_ E \_ PROPAGATED-QUALIFIZIERER \_**
</dt> <dd> <dl> <dt>

2147749915 (0x8004101B)
</dt> <dt>



Der Benutzer hat versucht, einen Qualifizierer zu löschen, der nicht im Besitz von war. Der Qualifizierer wurde von einer übergeordneten Klasse vererbt.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROPAGATED_PROPERTY"></span><span id="wbem_e_propagated_property"></span>**WBEM \_ E \_ PROPAGATED-EIGENSCHAFT \_**
</dt> <dd> <dl> <dt>

2147749916 (0x8004101C)
</dt> <dt>



Der Benutzer hat versucht, eine Eigenschaft zu löschen, die nicht im Besitz von war. Die Eigenschaft wurde von einer übergeordneten Klasse vererbt.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNEXPECTED"></span><span id="wbem_e_unexpected"></span>**WBEM \_ E \_ UNEXPECTED**
</dt> <dd> <dl> <dt>

2147749917 (0x8004101D)
</dt> <dt>



Der Client hat eine unerwartete und unzulässige Sequenz von Aufrufen vorgenommen, z. B. das Aufrufen von [**EndEnumeration**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-endenumeration) vor dem Aufruf von [**BeginEnumeration.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-beginenumeration)


</dt> </dl> </dd> <dt>

<span id="WBEM_E_ILLEGAL_OPERATION"></span><span id="wbem_e_illegal_operation"></span>**WBEM \_ E \_ ILLEGAL \_ OPERATION**
</dt> <dd> <dl> <dt>

2147749918 (0x8004101E)
</dt> <dt>



Der Benutzer hat einen unzulässigen Vorgang angefordert, z. B. das Erstellen einer Klasse aus einer -Instanz.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CANNOT_BE_KEY"></span><span id="wbem_e_cannot_be_key"></span>**WBEM \_ E KANN KEIN SCHLÜSSEL \_ \_ \_ SEIN**
</dt> <dd> <dl> <dt>

2147749919 (0x8004101F)
</dt> <dt>



Unzulässiger Versuch, einen Schlüsselqualifizierer für eine Eigenschaft anzugeben, die kein Schlüssel sein darf. Die Schlüssel sind in der Klassendefinition für ein Objekt angegeben und können nicht für jede Instanz einzeln geändert werden.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INCOMPLETE_CLASS"></span><span id="wbem_e_incomplete_class"></span>**WBEM \_ E \_ \_ INCOMPLETE-KLASSE**
</dt> <dd> <dl> <dt>

2147749920 (0x80041020)
</dt> <dt>



Das aktuelle Objekt ist keine gültige Klassendefinition. Entweder ist sie unvollständig, oder sie wurde nicht mithilfe von [**SWbemObject.Put \_**](swbemobject-put-.md)bei WMI registriert.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_SYNTAX"></span><span id="wbem_e_invalid_syntax"></span>**WBEM \_ E \_ UNGÜLTIGE \_ SYNTAX**
</dt> <dd> <dl> <dt>

2147749921 (0x80041021)
</dt> <dt>



Die Abfrage ist syntaktisch ungültig.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NONDECORATED_OBJECT"></span><span id="wbem_e_nondecorated_object"></span>**WBEM \_ E \_ NONDECORATED \_ OBJECT**
</dt> <dd> <dl> <dt>

2147749922 (0x80041022)
</dt> <dt>



Für die zukünftige Verwendung reserviert.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_READ_ONLY"></span><span id="wbem_e_read_only"></span>**WBEM \_ E \_ READ \_ ONLY**
</dt> <dd> <dl> <dt>

2147749923 (0x80041023)
</dt> <dt>



Es wurde versucht, eine schreibgeschützte Eigenschaft zu ändern.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_NOT_CAPABLE"></span><span id="wbem_e_provider_not_capable"></span>**WBEM \_ E \_ PROVIDER \_ NOT \_ CAPABLE**
</dt> <dd> <dl> <dt>

2147749924 (0x80041024)
</dt> <dt>



Der Anbieter kann den angeforderten Vorgang nicht ausführen. Dies kann eine zu komplexe Abfrage, das Abrufen einer Instanz, das Erstellen oder Aktualisieren einer Klasse, das Löschen einer Klasse oder das Aufzählen einer Klasse umfassen.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CLASS_HAS_CHILDREN"></span><span id="wbem_e_class_has_children"></span>**WBEM \_ \_ E-KLASSE VERFÜGT \_ ÜBER \_ CHILDREN**
</dt> <dd> <dl> <dt>

2147749925 (0x80041025)
</dt> <dt>



Es wurde versucht, eine Änderung zu machen, die eine Unterklasse für ungültig erklärt.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CLASS_HAS_INSTANCES"></span><span id="wbem_e_class_has_instances"></span>**WBEM \_ \_ E-KLASSE \_ VERFÜGT \_ ÜBER INSTANZEN**
</dt> <dd> <dl> <dt>

2147749926 (0x80041026)
</dt> <dt>



Es wurde versucht, eine Klasse mit -Instanzen zu löschen oder zu ändern.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_QUERY_NOT_IMPLEMENTED"></span><span id="wbem_e_query_not_implemented"></span>**WBEM E QUERY NOT IMPLEMENTED (WBEM \_ \_ \_ E-ABFRAGE NICHT \_ IMPLEMENTIERT)**
</dt> <dd> <dl> <dt>

2147749927 (0x80041027)
</dt> <dt>



Für die zukünftige Verwendung reserviert.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_ILLEGAL_NULL"></span><span id="wbem_e_illegal_null"></span>**WBEM \_ E \_ ILLEGAL \_ NULL**
</dt> <dd> <dl> <dt>

2147749928 (0x80041028)
</dt> <dt>



Der Wert **Nothing/NULL** wurde für eine Eigenschaft angegeben, die einen Wert haben muss, z. B. einen Wert, der durch einen [**Schlüssel-,**](key-qualifier.md) [**indizierten**](optional-qualifiers.md)oder **Not NULL-Qualifizierer \_** gekennzeichnet ist.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_QUALIFIER_TYPE"></span><span id="wbem_e_invalid_qualifier_type"></span>**WBEM \_ E \_ UNGÜLTIGER \_ QUALIFIZIERERTYP \_**
</dt> <dd> <dl> <dt>

2147749929 (0x80041029)
</dt> <dt>



Ein Variant-Wert für einen Qualifizierer wurde bereitgestellt, der kein legaler Qualifizierertyp ist.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_PROPERTY_TYPE"></span><span id="wbem_e_invalid_property_type"></span>**WBEM \_ E \_ UNGÜLTIGER \_ \_ EIGENSCHAFTENTYP**
</dt> <dd> <dl> <dt>

2147749930 (0x8004102A)
</dt> <dt>



Der für eine Eigenschaft angegebene CIM-Typ ist ungültig.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_VALUE_OUT_OF_RANGE"></span><span id="wbem_e_value_out_of_range"></span>**WBEM \_ E \_ VALUE \_ OUT \_ OF \_ RANGE**
</dt> <dd> <dl> <dt>

2147749931 (0x8004102B)
</dt> <dt>



Die Anforderung wurde mit einem Wert vorgenommen, der nicht im bereich liegt, oder sie ist nicht mit dem Typ kompatibel.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CANNOT_BE_SINGLETON"></span><span id="wbem_e_cannot_be_singleton"></span>**WBEM \_ E KANN NICHT \_ \_ \_ SINGLETON SEIN**
</dt> <dd> <dl> <dt>

2147749932 (0x8004102C)
</dt> <dt>



Es wurde ein unzulässiger Versuch unternommen, ein Klassen-Singleton zu machen, z. B. wenn die Klasse von einer Nicht-Singletonklasse abgeleitet ist.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_CIM_TYPE"></span><span id="wbem_e_invalid_cim_type"></span>**WBEM \_ E \_ UNGÜLTIGER \_ \_ CIM-TYP**
</dt> <dd> <dl> <dt>

2147749933 (0x8004102D)
</dt> <dt>



Der angegebene CIM-Typ ist ungültig.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_METHOD"></span><span id="wbem_e_invalid_method"></span>**WBEM \_ E \_ INVALID \_ METHOD**
</dt> <dd> <dl> <dt>

2147749934 (0x8004102E)
</dt> <dt>



Die angeforderte Methode ist nicht verfügbar.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_METHOD_PARAMETERS"></span><span id="wbem_e_invalid_method_parameters"></span>**WBEM \_ E \_ UNGÜLTIGE \_ \_ METHODENPARAMETER**
</dt> <dd> <dl> <dt>

2147749935 (0x8004102F)
</dt> <dt>



Für die -Methode bereitgestellte Parameter sind ungültig.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_SYSTEM_PROPERTY"></span><span id="wbem_e_system_property"></span>**WBEM \_ \_ E-SYSTEMEIGENSCHAFT \_**
</dt> <dd> <dl> <dt>

2147749936 (0x80041030)
</dt> <dt>



Es wurde versucht, Qualifizierer für eine Systemeigenschaft abzurufen.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_PROPERTY"></span><span id="wbem_e_invalid_property"></span>**WBEM \_ E \_ UNGÜLTIGE \_ EIGENSCHAFT**
</dt> <dd> <dl> <dt>

2147749937 (0x80041031)
</dt> <dt>



Der Eigenschaftstyp wird nicht erkannt.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CALL_CANCELLED"></span><span id="wbem_e_call_cancelled"></span>**WBEM \_ E \_ CALL \_ CANCELLED**
</dt> <dd> <dl> <dt>

2147749938 (0x80041032)
</dt> <dt>



Der asynchrone Prozess wurde intern oder vom Benutzer abgebrochen. Beachten Sie, dass der Vorgang aufgrund des zeitlichen Ablaufs und der Art des asynchronen Vorgangs möglicherweise nicht wirklich abgebrochen wurde.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_SHUTTING_DOWN"></span><span id="wbem_e_shutting_down"></span>**WBEM \_ E \_ WIRD \_ HERUNTERGEFAHREN**
</dt> <dd> <dl> <dt>

2147749939 (0x80041033)
</dt> <dt>



Der Benutzer hat einen Vorgang angefordert, während WMI gerade heruntergefahren wird.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROPAGATED_METHOD"></span><span id="wbem_e_propagated_method"></span>**WBEM \_ E \_ PROPAGATED-METHODE \_**
</dt> <dd> <dl> <dt>

2147749940 (0x80041034)
</dt> <dt>



Es wurde versucht, einen vorhandenen Methodennamen aus einer übergeordneten Klasse wiederzuverwenden, und die Signaturen stimmen nicht überein.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNSUPPORTED_PARAMETER"></span><span id="wbem_e_unsupported_parameter"></span>**NICHT UNTERSTÜTZTER WBEM \_ \_ \_ E-PARAMETER**
</dt> <dd> <dl> <dt>

2147749941 (0x80041035)
</dt> <dt>



Mindestens ein Parameterwert (z. B. ein Abfragetext) ist zu komplex oder wird nicht unterstützt. WMI wird daher aufgefordert, den Vorgang mit einfacheren Parametern zu wiederholen.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_MISSING_PARAMETER_ID"></span><span id="wbem_e_missing_parameter_id"></span>**WBEM \_ E \_ FEHLENDE \_ \_ PARAMETER-ID**
</dt> <dd> <dl> <dt>

2147749942 (0x80041036)
</dt> <dt>



Der Parameter fehlte im Methodenaufruf.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_PARAMETER_ID"></span><span id="wbem_e_invalid_parameter_id"></span>**WBEM \_ E \_ INVALID \_ PARAMETER \_ ID**
</dt> <dd> <dl> <dt>

2147749943 (0x80041037)
</dt> <dt>



Der Methodenparameter verfügt über einen [**ungültigen ID-Qualifizierer.**](standard-wmi-qualifiers.md)


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NONCONSECUTIVE_PARAMETER_IDS"></span><span id="wbem_e_nonconsecutive_parameter_ids"></span>**WBEM \_ E \_ NONCONSECUTIVE \_ PARAMETER \_ IDS**
</dt> <dd> <dl> <dt>

2147749944 (0x80041038)
</dt> <dt>



Mindestens einer der Methodenparameter weist [**ID-Qualifizierer**](standard-wmi-qualifiers.md) auf, die nicht sequenzierend sind.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PARAMETER_ID_ON_RETVAL"></span><span id="wbem_e_parameter_id_on_retval"></span>**WBEM \_ E \_ PARAMETER \_ ID \_ ON \_ RETVAL**
</dt> <dd> <dl> <dt>

2147749945 (0x80041039)
</dt> <dt>



Der Rückgabewert für [](standard-wmi-qualifiers.md) eine Methode verfügt über einen ID-Qualifizierer.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_OBJECT_PATH"></span><span id="wbem_e_invalid_object_path"></span>**WBEM \_ E \_ UNGÜLTIGER \_ \_ OBJEKTPFAD**
</dt> <dd> <dl> <dt>

2147749946 (0x8004103A)
</dt> <dt>



Der angegebene Objektpfad war ungültig.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_OUT_OF_DISK_SPACE"></span><span id="wbem_e_out_of_disk_space"></span>**WBEM \_ E NICHT GENÜGEND \_ \_ \_ \_ SPEICHERPLATZ**
</dt> <dd> <dl> <dt>

2147749947 (0x8004103B)
</dt> <dt>



Der Datenträger hat nicht genügend Speicherplatz, oder die Größe des WMI-Repositorys (CIM-Repository) von 4 GB wird erreicht.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_BUFFER_TOO_SMALL"></span><span id="wbem_e_buffer_too_small"></span>**WBEM \_ E \_ BUFFER \_ TOO \_ SMALL**
</dt> <dd> <dl> <dt>

2147749948 (0x8004103C)
</dt> <dt>



Der bereitgestellte Puffer war zu klein, um alle Objekte im Enumerator zu speichern oder eine Zeichenfolgeneigenschaft zu lesen.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNSUPPORTED_PUT_EXTENSION"></span><span id="wbem_e_unsupported_put_extension"></span>**WBEM \_ E NICHT UNTERSTÜTZTE \_ \_ \_ PUT-ERWEITERUNG**
</dt> <dd> <dl> <dt>

2147749949 (0x8004103D)
</dt> <dt>



Der Anbieter unterstützt den angeforderten Put-Vorgang nicht.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNKNOWN_OBJECT_TYPE"></span><span id="wbem_e_unknown_object_type"></span>**WBEM \_ E \_ UNBEKANNTER \_ \_ OBJEKTTYP**
</dt> <dd> <dl> <dt>

2147749950 (0x8004103E)
</dt> <dt>



Beim Marshalling wurde ein Objekt mit einem falschen Typ oder einer falschen Version gefunden.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNKNOWN_PACKET_TYPE"></span><span id="wbem_e_unknown_packet_type"></span>**WBEM \_ E \_ UNBEKANNTER \_ \_ PAKETTYP**
</dt> <dd> <dl> <dt>

2147749951 (0x8004103F)
</dt> <dt>



Beim Marshalling wurde ein Paket mit einem falschen Typ oder einer falschen Version gefunden.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_MARSHAL_VERSION_MISMATCH"></span><span id="wbem_e_marshal_version_mismatch"></span>**WBEM \_ E \_ MARSHAL \_ VERSION \_ MISMATCH**
</dt> <dd> <dl> <dt>

2147749952 (0x80041040)
</dt> <dt>



Das Paket verfügt über eine nicht unterstützte Version.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_MARSHAL_INVALID_SIGNATURE"></span><span id="wbem_e_marshal_invalid_signature"></span>**WBEM \_ E \_ MARSHALLAL \_ UNGÜLTIGE \_ SIGNATUR**
</dt> <dd> <dl> <dt>

2147749953 (0x80041041)
</dt> <dt>



Das Paket scheint beschädigt zu sein.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_QUALIFIER"></span><span id="wbem_e_invalid_qualifier"></span>**WBEM \_ E \_ \_ UNGÜLTIGER QUALIFIZIERER**
</dt> <dd> <dl> <dt>

2147749954 (0x80041042)
</dt> <dt>



Es wurde versucht, nicht übereinstimmende Qualifizierer zu verwenden, z. B. schlüssel für ein Objekt anstelle einer Eigenschaft zu \[ \] setzen.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_DUPLICATE_PARAMETER"></span><span id="wbem_e_invalid_duplicate_parameter"></span>**WBEM \_ E \_ UNGÜLTIGER \_ DOPPELTER \_ PARAMETER**
</dt> <dd> <dl> <dt>

2147749955 (0x80041043)
</dt> <dt>



Doppelter Parameter wurde in einer CIM-Methode deklariert.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_TOO_MUCH_DATA"></span><span id="wbem_e_too_much_data"></span>**WBEM \_ E ZU VIELE \_ \_ \_ DATEN**
</dt> <dd> <dl> <dt>

2147749956 (0x80041044)
</dt> <dt>



Für die zukünftige Verwendung reserviert.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_SERVER_TOO_BUSY"></span><span id="wbem_e_server_too_busy"></span>**\_WBEM-E-SERVER \_ \_ ZU \_ AUSGELASTET**
</dt> <dd> <dl> <dt>

2147749957 (0x80041045)
</dt> <dt>



Aufruf von [**IWbemObjectSink::Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) ist fehlgeschlagen. Der Anbieter kann das Ereignis erneut losgehen.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_FLAVOR"></span><span id="wbem_e_invalid_flavor"></span>**WBEM \_ E \_ INVALID \_ FLAVOR**
</dt> <dd> <dl> <dt>

2147749958 (0x80041046)
</dt> <dt>



Die angegebene Qualifizierer-Variante war ungültig.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CIRCULAR_REFERENCE"></span><span id="wbem_e_circular_reference"></span>**WBEM \_ E \_ CIRCULAR \_ REFERENCE**
</dt> <dd> <dl> <dt>

2147749959 (0x80041047)
</dt> <dt>



Es wurde versucht, einen Verweis zu erstellen, der kreisförmig ist (z. B. eine Klasse von sich selbst ableiten).


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNSUPPORTED_CLASS_UPDATE"></span><span id="wbem_e_unsupported_class_update"></span>**WBEM \_ E \_ UNSUPPORTED \_ CLASS \_ UPDATE**
</dt> <dd> <dl> <dt>

2147749960 (0x80041048)
</dt> <dt>



Die angegebene Klasse wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CANNOT_CHANGE_KEY_INHERITANCE"></span><span id="wbem_e_cannot_change_key_inheritance"></span>**WBEM \_ E \_ KANN \_ \_ \_ SCHLÜSSELVERERBUNG NICHT ÄNDERN**
</dt> <dd> <dl> <dt>

2147749961 (0x80041049)
</dt> <dt>



Es wurde versucht, einen Schlüssel zu ändern, wenn Instanzen oder Unterklassen den Schlüssel bereits verwenden.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CANNOT_CHANGE_INDEX_INHERITANCE"></span><span id="wbem_e_cannot_change_index_inheritance"></span>**WBEM \_ E \_ KANN \_ \_ \_ INDEXVERERBUNG NICHT ÄNDERN**
</dt> <dd> <dl> <dt>

2147749968 (0x80041050)
</dt> <dt>



Es wurde versucht, einen Index zu ändern, wenn Instanzen oder Unterklassen den Index bereits verwenden.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_TOO_MANY_PROPERTIES"></span><span id="wbem_e_too_many_properties"></span>**WBEM \_ E ZU VIELE \_ \_ \_ EIGENSCHAFTEN**
</dt> <dd> <dl> <dt>

2147749969 (0x80041051)
</dt> <dt>



Es wurde versucht, mehr Eigenschaften zu erstellen, als die aktuelle Version der -Klasse unterstützt.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UPDATE_TYPE_MISMATCH"></span><span id="wbem_e_update_type_mismatch"></span>**WBEM \_ E \_ UPDATE \_ TYPE \_ MISMATCH**
</dt> <dd> <dl> <dt>

2147749970 (0x80041052)
</dt> <dt>



Die Eigenschaft wurde mit einem in Konflikt geratenen Typ in einer abgeleiteten Klasse neu definiert.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UPDATE_OVERRIDE_NOT_ALLOWED"></span><span id="wbem_e_update_override_not_allowed"></span>**WBEM \_ E \_ UPDATE \_ OVERRIDE \_ NOT \_ ALLOWED**
</dt> <dd> <dl> <dt>

2147749971 (0x80041053)
</dt> <dt>



In einer abgeleiteten Klasse wurde versucht, einen Qualifizierer zu überschreiben, der nicht überschrieben werden kann.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UPDATE_PROPAGATED_METHOD"></span><span id="wbem_e_update_propagated_method"></span>**WBEM \_ E \_ UPDATE \_ PROPAGATED-METHODE \_**
</dt> <dd> <dl> <dt>

2147749972 (0x80041054)
</dt> <dt>



Die Methode wurde mit einer in Konfliktstehenden Signatur in einer abgeleiteten Klasse erneut deklariert.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_METHOD_NOT_IMPLEMENTED"></span><span id="wbem_e_method_not_implemented"></span>**WBEM \_ \_ E-METHODE \_ NICHT \_ IMPLEMENTIERT**
</dt> <dd> <dl> <dt>

2147749973 (0x80041055)
</dt> <dt>



Es wurde versucht, eine Methode auszuführen, die nicht mit \[ gekennzeichnet \] ist, die in einer relevanten Klasse implementiert ist.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_METHOD_DISABLED"></span><span id="wbem_e_method_disabled"></span>**WBEM \_ \_ E-METHODE \_ DEAKTIVIERT**
</dt> <dd> <dl> <dt>


</dt> <dt>



Es wurde versucht, eine Methode auszuführen, die mit deaktivierter markiert \[ \] ist.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_REFRESHER_BUSY"></span><span id="wbem_e_refresher_busy"></span>**WBEM \_ E \_ REFRESHER \_ BUSY**
</dt> <dd> <dl> <dt>

2147749975 (0x80041057)
</dt> <dt>



Refresher ist mit einem anderen Vorgang ausgelastet.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNPARSABLE_QUERY"></span><span id="wbem_e_unparsable_query"></span>**WBEM \_ E \_ UNPARSABLE \_ QUERY**
</dt> <dd> <dl> <dt>

2147749976 (0x80041058)
</dt> <dt>



Die Filterabfrage ist syntaktisch ungültig.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NOT_EVENT_CLASS"></span><span id="wbem_e_not_event_class"></span>**WBEM \_ E \_ \_ NOT-EREIGNISKLASSE \_**
</dt> <dd> <dl> <dt>

2147749977 (0x80041059)
</dt> <dt>



Die FROM-Klausel einer Filterabfrage verweist auf eine Klasse, die keine Ereignisklasse ist (nicht von [**\_ \_ Event abgeleitet).**](--event.md)


</dt> </dl> </dd> <dt>

<span id="WBEM_E_MISSING_GROUP_WITHIN"></span><span id="wbem_e_missing_group_within"></span>**WBEM \_ E \_ MISSING \_ GROUP \_ WITHIN**
</dt> <dd> <dl> <dt>

2147749978 (0x8004105A)
</dt> <dt>



Eine GROUP BY-Klausel wurde ohne die entsprechende GROUP WITHIN-Klausel verwendet.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_MISSING_AGGREGATION_LIST"></span><span id="wbem_e_missing_aggregation_list"></span>**WBEM \_ E \_ MISSING \_ AGGREGATION \_ LIST**
</dt> <dd> <dl> <dt>

2147749979 (0x8004105B)
</dt> <dt>



Es wurde eine GROUP BY-Klausel verwendet. Die Aggregation für alle Eigenschaften wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROPERTY_NOT_AN_OBJECT"></span><span id="wbem_e_property_not_an_object"></span>**WBEM \_ \_ E-EIGENSCHAFT \_ KEIN \_ \_ OBJEKT**
</dt> <dd> <dl> <dt>

2147749980 (0x8004105C)
</dt> <dt>



Für eine Eigenschaft, die kein eingebettetes Objekt ist, wurde Punktnotation verwendet.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_AGGREGATING_BY_OBJECT"></span><span id="wbem_e_aggregating_by_object"></span>**WBEM \_ E \_ AGGREGIEREN \_ NACH \_ OBJEKT**
</dt> <dd> <dl> <dt>

2147749981 (0x8004105D)
</dt> <dt>



Eine GROUP BY-Klausel verweist auf eine Eigenschaft, bei der es sich um ein eingebettetes Objekt ohne Verwendung der Punktnotation handelt.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNINTERPRETABLE_PROVIDER_QUERY"></span><span id="wbem_e_uninterpretable_provider_query"></span>**WBEM \_ E \_ UNINTERPRETABLE \_ PROVIDER \_ QUERY**
</dt> <dd> <dl> <dt>

2147749983 (0x8004105F)
</dt> <dt>



Die Ereignisanbieter-Registrierungsabfrage ([**\_ \_ EventProviderRegistration**](--eventproviderregistration.md)) hat nicht die Klassen angegeben, für die Ereignisse bereitgestellt wurden.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_BACKUP_RESTORE_WINMGMT_RUNNING"></span><span id="wbem_e_backup_restore_winmgmt_running"></span>**WBEM \_ E BACKUP RESTORE \_ \_ \_ WINMGMT \_ WIRD AUSGEFÜHRT**
</dt> <dd> <dl> <dt>

2147749984 (0x80041060)
</dt> <dt>



Es wurde eine Anforderung zum Sichern oder Wiederherstellen des Repositorys gestellt, während es von WinMgmt.exe oder vom SVCHOST-Prozess verwendet wurde, der den WMI-Dienst enthält.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_QUEUE_OVERFLOW"></span><span id="wbem_e_queue_overflow"></span>**WBEM \_ E \_ QUEUE \_ OVERFLOW**
</dt> <dd> <dl> <dt>

2147749985 (0x80041061)
</dt> <dt>



Die asynchrone Übermittlungswarteschlange ist überlaufen, da der Ereignis consumer zu langsam war.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PRIVILEGE_NOT_HELD"></span><span id="wbem_e_privilege_not_held"></span>**WBEM \_ \_ E-BERECHTIGUNG \_ NICHT \_ PRIVILEG**
</dt> <dd> <dl> <dt>

2147749986 (0x80041062)
</dt> <dt>



Fehler beim Vorgang, da der Client nicht über die erforderlichen Sicherheitsberechtigungen verfügen hat.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_OPERATOR"></span><span id="wbem_e_invalid_operator"></span>**WBEM \_ E \_ INVALID \_ OPERATOR**
</dt> <dd> <dl> <dt>

2147749987 (0x80041063)
</dt> <dt>



Der Operator ist für diesen Eigenschaftentyp ungültig.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_LOCAL_CREDENTIALS"></span><span id="wbem_e_local_credentials"></span>**LOKALE \_ WBEM-ANMELDEINFORMATIONEN \_ \_**
</dt> <dd> <dl> <dt>

2147749988 (0x80041064)
</dt> <dt>



Der Benutzer hat einen Benutzernamen/ein Kennwort/eine Autorität für eine lokale Verbindung angegeben. Der Benutzer muss einen leeren Benutzernamen bzw. ein leeres Kennwort verwenden und sich auf die Standardsicherheit verlassen.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CANNOT_BE_ABSTRACT"></span><span id="wbem_e_cannot_be_abstract"></span>**WBEM \_ E KANN NICHT \_ \_ ABSTRAKT \_ SEIN**
</dt> <dd> <dl> <dt>

2147749989 (0x80041065)
</dt> <dt>



Die Klasse wurde abstrakt gemacht, wenn ihre übergeordnete Klasse nicht abstrakt ist.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_AMENDED_OBJECT"></span><span id="wbem_e_amended_object"></span>**WBEM \_ \_ E-ÄNDERUNGSOBJEKT \_**
</dt> <dd> <dl> <dt>

2147749990 (0x80041066)
</dt> <dt>



Das geänderte Objekt wurde geschrieben, ohne dass das **Flag WBEM \_ FLAG USE AMENDED \_ \_ \_ QUALIFIERS** angegeben wurde.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CLIENT_TOO_SLOW"></span><span id="wbem_e_client_too_slow"></span>**WBEM E CLIENT TOO SLOW (WBEM \_ \_ E-CLIENT \_ ZU \_ LANGSAM)**
</dt> <dd> <dl> <dt>

2147749991 (0x80041067)
</dt> <dt>



Der Client hat Objekte nicht schnell genug aus einer Enumeration abgerufen. Diese Konstante wird zurückgegeben, wenn ein Client ein Enumerationsobjekt erstellt, aber objekte nicht rechtzeitig aus dem Enumerator abruft, was dazu führt, dass die Objektcaches des Enumerators sichern.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NULL_SECURITY_DESCRIPTOR"></span><span id="wbem_e_null_security_descriptor"></span>**WBEM \_ E \_ NULL \_ SECURITY \_ DESCRIPTOR**
</dt> <dd> <dl> <dt>

2147749992 (0x80041068)
</dt> <dt>



Es wurde ein NULL-Sicherheitsdeskriptor verwendet.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_TIMED_OUT"></span><span id="wbem_e_timed_out"></span>**WBEM \_ E \_ TIMED \_ OUT**
</dt> <dd> <dl> <dt>

2147749993 (0x80041069)
</dt> <dt>



Time out des Vorgangs.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_ASSOCIATION"></span><span id="wbem_e_invalid_association"></span>**WBEM \_ E \_ UNGÜLTIGE \_ ZUORDNUNG**
</dt> <dd> <dl> <dt>

2147749994
</dt> <dt>



Die Zuordnung ist ungültig.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_AMBIGUOUS_OPERATION"></span><span id="wbem_e_ambiguous_operation"></span>**WBEM \_ E \_ MEHRDEUTIGER \_ VORGANG**
</dt> <dd> <dl> <dt>

2147749995 (0x8004106B)
</dt> <dt>



Der Vorgang war mehrdeutig.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_QUOTA_VIOLATION"></span><span id="wbem_e_quota_violation"></span>**WBEM \_ \_ E-KONTINGENTVERLETZUNG \_**
</dt> <dd> <dl> <dt>

2147749996 (0x8004106C)
</dt> <dt>



WMI nimmt zu viel Arbeitsspeicher ein. Dies kann durch eine geringe Arbeitsspeicherverfügbarkeit oder einen übermäßigen Arbeitsspeicherverbrauch durch WMI verursacht werden.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_TRANSACTION_CONFLICT"></span><span id="wbem_e_transaction_conflict"></span>**WBEM \_ E \_ TRANSACTION \_ CONFLICT**
</dt> <dd> <dl> <dt>

2147749997 (0x8004106D)
</dt> <dt>



Der Vorgang führte zu einem Transaktionskonflikt.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_FORCED_ROLLBACK"></span><span id="wbem_e_forced_rollback"></span>**WBEM \_ E \_ FORCED \_ ROLLBACK**
</dt> <dd> <dl> <dt>

2147749998 (0x8004106E)
</dt> <dt>



Die Transaktion hat einen Rollback erzwungen.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNSUPPORTED_LOCALE"></span><span id="wbem_e_unsupported_locale"></span>**WBEM \_ E \_ UNSUPPORTED \_ LOCALE**
</dt> <dd> <dl> <dt>

2147749999 (0x8004106F)
</dt> <dt>



Das im Aufruf verwendete Locale wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_HANDLE_OUT_OF_DATE"></span><span id="wbem_e_handle_out_of_date"></span>**WBEM \_ E \_ HANDLE \_ VERALTET \_ \_**
</dt> <dd> <dl> <dt>

2147750000 (0x80041070)
</dt> <dt>



Das Objekthand handle ist veraltet.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CONNECTION_FAILED"></span><span id="wbem_e_connection_failed"></span>**FEHLER BEI WBEM \_ \_ \_ E-VERBINDUNG**
</dt> <dd> <dl> <dt>

2147750001 (0x80041071)
</dt> <dt>



Fehler beim Herstellen SQL Datenbank.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_HANDLE_REQUEST"></span><span id="wbem_e_invalid_handle_request"></span>**WBEM \_ E \_ INVALID \_ HANDLE \_ REQUEST**
</dt> <dd> <dl> <dt>

2147750002 (0x80041072)
</dt> <dt>



Die Handleanforderung war ungültig.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROPERTY_NAME_TOO_WIDE"></span><span id="wbem_e_property_name_too_wide"></span>**WBEM \_ \_ E-EIGENSCHAFTENNAME \_ \_ ZU \_ BREIT**
</dt> <dd> <dl> <dt>

2147750003 (0x80041073)
</dt> <dt>



Der Eigenschaftenname enthält mehr als 255 Zeichen.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CLASS_NAME_TOO_WIDE"></span><span id="wbem_e_class_name_too_wide"></span>**WBEM \_ \_ E-KLASSENNAME \_ \_ ZU \_ BREIT**
</dt> <dd> <dl> <dt>

2147750004 (0x80041074)
</dt> <dt>



Der Klassenname enthält mehr als 255 Zeichen.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_METHOD_NAME_TOO_WIDE"></span><span id="wbem_e_method_name_too_wide"></span>**WBEM \_ \_ E-METHODENNAME \_ \_ ZU \_ BREIT**
</dt> <dd> <dl> <dt>

2147750005 (0x80041075)
</dt> <dt>



Der Methodenname enthält mehr als 255 Zeichen.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_QUALIFIER_NAME_TOO_WIDE"></span><span id="wbem_e_qualifier_name_too_wide"></span>**WBEM \_ \_ E-QUALIFIZIERERNAME \_ \_ ZU \_ BREIT**
</dt> <dd> <dl> <dt>

2147750006 (0x80041076)
</dt> <dt>



Der Qualifizierername enthält mehr als 255 Zeichen.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_RERUN_COMMAND"></span><span id="wbem_e_rerun_command"></span>**BEFEHL "WBEM \_ E \_ \_ RERUN"**
</dt> <dd> <dl> <dt>

2147750007 (0x80041077)
</dt> <dt>



Der SQL befehl muss erneut ausgeführt werden, da ein Deadlock in der SQL. Dies kann nur zurückgegeben werden, wenn Daten in einer Datenbank SQL werden.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_DATABASE_VER_MISMATCH"></span><span id="wbem_e_database_ver_mismatch"></span>**WBEM \_ E \_ DATABASE \_ VER \_ MISMATCH**
</dt> <dd> <dl> <dt>

2147750008 (0x80041078)
</dt> <dt>



Die Datenbankversion ist nicht mit der Version übereinstimmen, die der Repositorytreiber verarbeitet.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_VETO_DELETE"></span><span id="wbem_e_veto_delete"></span>**WBEM \_ E \_ EMAIL \_ DELETE**
</dt> <dd> <dl> <dt>

2147750009 (0x80041079)
</dt> <dt>



WMI kann den Löschvorgang nicht ausführen, da er vom Anbieter nicht zulässig ist.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_VETO_PUT"></span><span id="wbem_e_veto_put"></span>**WBEM \_ E \_ WIE PUT \_**
</dt> <dd> <dl> <dt>

2147750010 (0x8004107A)
</dt> <dt>



WMI kann den Put-Vorgang nicht ausführen, da er vom Anbieter nicht zulässig ist.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_LOCALE"></span><span id="wbem_e_invalid_locale"></span>**WBEM \_ E \_ \_ UNGÜLTIGES LOCALE**
</dt> <dd> <dl> <dt>

2147750016 (0x80041080)
</dt> <dt>



Der angegebene Locale Identifier war für den Vorgang ungültig.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_SUSPENDED"></span><span id="wbem_e_provider_suspended"></span>**WBEM \_ E \_ PROVIDER \_ SUSPENDED**
</dt> <dd> <dl> <dt>

2147750017 (0x80041081)
</dt> <dt>



Der Anbieter wird angehalten.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_SYNCHRONIZATION_REQUIRED"></span><span id="wbem_e_synchronization_required"></span>**WBEM \_ \_ E-SYNCHRONISIERUNG \_ ERFORDERLICH**
</dt> <dd> <dl> <dt>

2147750018 (0x80041082)
</dt> <dt>



Das Objekt muss in das WMI-Repository geschrieben und erneut abgerufen werden, bevor der angeforderte Vorgang erfolgreich sein kann. Diese Konstante wird zurückgegeben, wenn für ein Objekt ein Committed und abruft werden muss, um den Eigenschaftswert zu sehen.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NO_SCHEMA"></span><span id="wbem_e_no_schema"></span>**WBEM \_ E \_ NO \_ SCHEMA**
</dt> <dd> <dl> <dt>

2147750019 (0x80041083)
</dt> <dt>



Der Vorgang kann nicht abgeschlossen werden. Es ist kein Schema verfügbar.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_ALREADY_REGISTERED"></span><span id="wbem_e_provider_already_registered"></span>**WBEM \_ E \_ PROVIDER \_ ALREADY \_ REGISTERED**
</dt> <dd> <dl> <dt>

02147750020 (0x119FD010)
</dt> <dt>



Der Anbieter kann nicht registriert werden, da er bereits registriert ist.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_NOT_REGISTERED"></span><span id="wbem_e_provider_not_registered"></span>**WBEM \_ E \_ PROVIDER \_ NOT \_ REGISTERED**
</dt> <dd> <dl> <dt>

2147750021 (0x80041085)
</dt> <dt>



Der Anbieter wurde nicht registriert.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_FATAL_TRANSPORT_ERROR"></span><span id="wbem_e_fatal_transport_error"></span>**WBEM \_ \_ E: \_ SCHWERWIEGENDER \_ TRANSPORTFEHLER**
</dt> <dd> <dl> <dt>

2147750022 (0x80041086)
</dt> <dt>



Schwerwiegender Transportfehler.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_ENCRYPTED_CONNECTION_REQUIRED"></span><span id="wbem_e_encrypted_connection_required"></span>**WBEM \_ E \_ \_ ENCRYPTED-VERBINDUNG \_ ERFORDERLICH**
</dt> <dd> <dl> <dt>

2147750023 (0x80041087)
</dt> <dt>



Der Benutzer hat versucht, einen Computernamen oder eine Domäne ohne verschlüsselte Verbindung festlegen.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_TIMED_OUT"></span><span id="wbem_e_provider_timed_out"></span>**TIME OUT DES WBEM \_ \_ \_ \_ E-ANBIETERS**
</dt> <dd> <dl> <dt>

2147750024 (0x80041088)
</dt> <dt>



Ein Anbieter konnte keine Ergebnisse innerhalb des angegebenen Timeouts melden.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NO_KEY"></span><span id="wbem_e_no_key"></span>**WBEM \_ E \_ NO \_ KEY**
</dt> <dd> <dl> <dt>

2147750025 (0x80041089)
</dt> <dt>



Der Benutzer hat versucht, eine Instanz ohne definierten Schlüssel zu erstellen.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_DISABLED"></span><span id="wbem_e_provider_disabled"></span>**WBEM \_ E \_ PROVIDER \_ DISABLED**
</dt> <dd> <dl> <dt>

2147750026 (0x8004108A)
</dt> <dt>



Der Benutzer hat versucht, eine Anbieterinstanz zu registrieren, aber der COM-Server für die Anbieterinstanz wurde entladen.


</dt> </dl> </dd> <dt>

<span id="WBEMESS_E_REGISTRATION_TOO_BROAD"></span><span id="wbemess_e_registration_too_broad"></span>**WBEMESS \_ \_ E-REGISTRIERUNG \_ ZU \_ BREIT**
</dt> <dd> <dl> <dt>

2147753985 (0x80042001)
</dt> <dt>



Die Anbieterregistrierung überschneidet sich mit der Systemereignisdomäne.


</dt> </dl> </dd> <dt>

<span id="WBEMESS_E_REGISTRATION_TOO_PRECISE"></span><span id="wbemess_e_registration_too_precise"></span>**WBEMESS \_ \_ E-REGISTRIERUNG \_ ZU \_ PRÄZISE**
</dt> <dd> <dl> <dt>

2147753986 (0x80042002)
</dt> <dt>



In dieser Abfrage wurde keine WITHIN-Klausel verwendet.


</dt> </dl> </dd> <dt>

<span id="WBEMESS_E_AUTHZ_NOT_PRIVILEGED"></span><span id="wbemess_e_authz_not_privileged"></span>**WBEMESS \_ E \_ OHNE BERECHTIGUNGEN \_ \_**
</dt> <dd> <dl> <dt>

2147753987 (0x80042003)
</dt> <dt>



Dieser Computer verfügt nicht über die erforderlichen Domänenberechtigungen zur Unterstützung der Sicherheitsfunktionen, die sich auf die erstellte Abonnementinstanz beziehen. Wenden Sie sich an den Domänenadministrator, um diesen Computer der Windows Autorisierungszugriffsgruppe hinzufügen zu lassen.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_RETRY_LATER"></span><span id="wbem_e_retry_later"></span>**WBEM \_ E \_ RETRY \_ LATER**
</dt> <dd> <dl> <dt>

2147758081 (0x80043001)
</dt> <dt>



Für die zukünftige Verwendung reserviert.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_RESOURCE_CONTENTION"></span><span id="wbem_e_resource_contention"></span>**WBEM \_ E \_ RESOURCE \_ CONTENTION**
</dt> <dd> <dl> <dt>

2147758082 (0x80043002)
</dt> <dt>



Für die zukünftige Verwendung reserviert.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_QUALIFIER_NAME"></span><span id="wbemmof_e_expected_qualifier_name"></span>**WBEMMOF \_ E \_ ERWARTETER \_ QUALIFIZIERERNAME \_**
</dt> <dd> <dl> <dt>

2147762177 (0x80044001)
</dt> <dt>



Ein Qualifizierername wurde erwartet.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_SEMI"></span><span id="wbemmof_e_expected_semi"></span>**WBEMMOF \_ E \_ ERWARTET \_ SEMI**
</dt> <dd> <dl> <dt>

2147762178 (0x80044002)
</dt> <dt>



Semikolon oder '=' wurde erwartet.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_OPEN_BRACE"></span><span id="wbemmof_e_expected_open_brace"></span>**WBEMMOF \_ E \_ ERWARTETE \_ GEÖFFNETE \_ GESCHWEIFTE KLAMMER**
</dt> <dd> <dl> <dt>

2147762179 (0x80044003)
</dt> <dt>



Es wurde eine öffnende geschweifte Klammer erwartet.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_CLOSE_BRACE"></span><span id="wbemmof_e_expected_close_brace"></span>**WBEMMOF \_ E \_ ERWARTET \_ SCHLIEßENDE \_ GESCHWEIFTE KLAMMER**
</dt> <dd> <dl> <dt>

2147762180 (0x80044004)
</dt> <dt>



Fehlende schließende geschweifte Klammer oder ein ungültiges Arrayelement.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_CLOSE_BRACKET"></span><span id="wbemmof_e_expected_close_bracket"></span>**WBEMMOF \_ E \_ ERWARTET \_ SCHLIEßENDE \_ KLAMMER**
</dt> <dd> <dl> <dt>

2147762181 (0x80044005)
</dt> <dt>



Es wurde eine schließende Klammer erwartet.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_CLOSE_PAREN"></span><span id="wbemmof_e_expected_close_paren"></span>**WBEMMOF \_ E ERWARTET CLOSE \_ \_ \_ PAREN**
</dt> <dd> <dl> <dt>

2147762182 (0x80044006)
</dt> <dt>



Schließende Klammer erwartet.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_ILLEGAL_CONSTANT_VALUE"></span><span id="wbemmof_e_illegal_constant_value"></span>**WBEMMOF \_ E \_ ILLEGAL \_ CONSTANT \_ VALUE**
</dt> <dd> <dl> <dt>

2147762183 (0x80044007)
</dt> <dt>



Numerischer Wert liegt nicht im Bereich oder Zeichenfolgen ohne Anführungszeichen.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_TYPE_IDENTIFIER"></span><span id="wbemmof_e_expected_type_identifier"></span>**WBEMMOF \_ E \_ ERWARTETER \_ \_ TYPBEZEICHNER**
</dt> <dd> <dl> <dt>

2147762184 (0x80044008)
</dt> <dt>



Ein Typbezeichner wurde erwartet.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_OPEN_PAREN"></span><span id="wbemmof_e_expected_open_paren"></span>**WBEMMOF \_ E ERWARTET OPEN \_ \_ \_ PAREN**
</dt> <dd> <dl> <dt>

2147762185 (0x80044009)
</dt> <dt>



Es wurde eine geöffnete Klammer erwartet.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_UNRECOGNIZED_TOKEN"></span><span id="wbemmof_e_unrecognized_token"></span>**WBEMMOF \_ E \_ UNRECOGNIZED \_ TOKEN**
</dt> <dd> <dl> <dt>

2147762186 (0x8004400A)
</dt> <dt>



Unerwartetes Token in der Datei.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_UNRECOGNIZED_TYPE"></span><span id="wbemmof_e_unrecognized_type"></span>**WBEMMOF \_ E \_ UNRECOGNIZED \_ TYPE**
</dt> <dd> <dl> <dt>

2147762187 (0x8004400B)
</dt> <dt>



Unbekannter oder nicht unterstützter Typbezeichner.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_PROPERTY_NAME"></span><span id="wbemmof_e_expected_property_name"></span>**WBEMMOF \_ E \_ ERWARTETER \_ \_ EIGENSCHAFTENNAME**
</dt> <dd> <dl> <dt>

2147762187 (0x8004400B)
</dt> <dt>



Erwarteter Eigenschafts- oder Methodenname.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_TYPEDEF_NOT_SUPPORTED"></span><span id="wbemmof_e_typedef_not_supported"></span>**WBEMMOF \_ E \_ TYPEDEF NICHT \_ \_ UNTERSTÜTZT**
</dt> <dd> <dl> <dt>

2147762189 (0x8004400D)
</dt> <dt>



Typedefs und aufzählte Typen werden nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_UNEXPECTED_ALIAS"></span><span id="wbemmof_e_unexpected_alias"></span>**WBEMMOF \_ E \_ UNEXPECTED \_ ALIAS**
</dt> <dd> <dl> <dt>

2147762190 (0x8004400E)
</dt> <dt>



Nur ein Verweis auf ein Klassenobjekt kann einen Aliaswert haben.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_UNEXPECTED_ARRAY_INIT"></span><span id="wbemmof_e_unexpected_array_init"></span>**WBEMMOF \_ E \_ UNEXPECTED \_ ARRAY \_ INIT**
</dt> <dd> <dl> <dt>

2147762191 (0x8004400F)
</dt> <dt>



Unerwartete Arrayin initialisierung. Arrays müssen mit deklariert \[ \] werden.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_AMENDMENT_SYNTAX"></span><span id="wbemmof_e_invalid_amendment_syntax"></span>**WBEMMOF \_ E \_ UNGÜLTIGE \_ ZUSATZSYNTAX \_**
</dt> <dd> <dl> <dt>

2147762192 (0x80044010)
</dt> <dt>



Die Syntax des Namespacepfads ist ungültig.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_DUPLICATE_AMENDMENT"></span><span id="wbemmof_e_invalid_duplicate_amendment"></span>**WBEMMOF \_ E \_ INVALID \_ DUPLICATE \_ AMENDMENT**
</dt> <dd> <dl> <dt>

2147762193 (0x80044011)
</dt> <dt>



Doppelte Zusatzspezifizierer.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_PRAGMA"></span><span id="wbemmof_e_invalid_pragma"></span>**WBEMMOF \_ E \_ INVALID \_ PRAGMA**
</dt> <dd> <dl> <dt>

2147762194 (0x80044012)
</dt> <dt>



[ \# auf pragma](pragma-namespace.md) muss ein gültiges Schlüsselwort folgen.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_NAMESPACE_SYNTAX"></span><span id="wbemmof_e_invalid_namespace_syntax"></span>**WBEMMOF \_ E \_ UNGÜLTIGE \_ NAMESPACESYNTAX \_**
</dt> <dd> <dl> <dt>

2147762195 (0x80044013)
</dt> <dt>



Die Syntax des Namespacepfads ist ungültig.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_CLASS_NAME"></span><span id="wbemmof_e_expected_class_name"></span>**WBEMMOF \_ E \_ ERWARTETER \_ \_ KLASSENNAME**
</dt> <dd> <dl> <dt>

2147762196 (0x80044014)
</dt> <dt>



Ein unerwartetes Zeichen im Klassennamen muss ein Bezeichner sein.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_TYPE_MISMATCH"></span><span id="wbemmof_e_type_mismatch"></span>**WBEMMOF \_ \_ E-TYPKONFLIKT \_**
</dt> <dd> <dl> <dt>

2147762197 (0x80044015)
</dt> <dt>



Der angegebene Wert kann nicht in den entsprechenden Typ festgelegt werden.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_ALIAS_NAME"></span><span id="wbemmof_e_expected_alias_name"></span>**WBEMMOF \_ E \_ ERWARTETER \_ \_ ALIASNAME**
</dt> <dd> <dl> <dt>

2147762198 (0x80044016)
</dt> <dt>



Auf das Dollarzeichen muss ein Aliasname als Bezeichner folgen.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_CLASS_DECLARATION"></span><span id="wbemmof_e_invalid_class_declaration"></span>**WBEMMOF \_ E \_ UNGÜLTIGE \_ \_ KLASSENDEKLARATION**
</dt> <dd> <dl> <dt>

2147762199 (0x80044017)
</dt> <dt>



Die Klassendeklaration ist ungültig.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_INSTANCE_DECLARATION"></span><span id="wbemmof_e_invalid_instance_declaration"></span>**WBEMMOF \_ E \_ UNGÜLTIGE \_ \_ INSTANZDEKLARATION**
</dt> <dd> <dl> <dt>

2147762200 (0x80044018)
</dt> <dt>



Die Instanzdeklaration ist ungültig. Er muss mit "Instanz von" beginnen.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_DOLLAR"></span><span id="wbemmof_e_expected_dollar"></span>**WBEMMOF \_ E \_ ERWARTETER \_ DOLLAR**
</dt> <dd> <dl> <dt>

2147762201 (0x80044019)
</dt> <dt>



Erwartetes Dollarzeichen. Ein Alias im Formular "$name" muss dem Schlüsselwort "as" folgen.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_CIMTYPE_QUALIFIER"></span><span id="wbemmof_e_cimtype_qualifier"></span>**WBEMMOF \_ E \_ \_ CIMTYPE-QUALIFIZIERER**
</dt> <dd> <dl> <dt>

2147762202 (0x8004401A)
</dt> <dt>



Der CIMTYPE-Qualifizierer kann nicht direkt in einer MOF-Datei angegeben werden. Verwenden Sie die Standardtyp-Notation.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_DUPLICATE_PROPERTY"></span><span id="wbemmof_e_duplicate_property"></span>**WBEMMOF \_ E \_ \_ DUPLICATE-EIGENSCHAFT**
</dt> <dd> <dl> <dt>

2147762203 (0x8004401B)
</dt> <dt>



In der MOF wurde ein doppelter Eigenschaftenname gefunden.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_NAMESPACE_SPECIFICATION"></span><span id="wbemmof_e_invalid_namespace_specification"></span>**WBEMMOF \_ E \_ INVALID \_ NAMESPACE \_ SPECIFICATION**
</dt> <dd> <dl> <dt>

2147762204 (0x8004401C)
</dt> <dt>



Die Namespacesyntax ist ungültig. Verweise auf andere Server sind nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_OUT_OF_RANGE"></span><span id="wbemmof_e_out_of_range"></span>**WBEMMOF \_ E LIEGT NICHT IM \_ \_ \_ BEREICH**
</dt> <dd> <dl> <dt>

2147762205 (0x8004401D)
</dt> <dt>



Der Wert liegt nicht im Bereich.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_FILE"></span><span id="wbemmof_e_invalid_file"></span>**WBEMMOF \_ E \_ UNGÜLTIGE \_ DATEI**
</dt> <dd> <dl> <dt>

2147762206 (0x8004401E)
</dt> <dt>



Die Datei ist keine gültige MOF-Textdatei oder binäre MOF-Datei.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_ALIASES_IN_EMBEDDED"></span><span id="wbemmof_e_aliases_in_embedded"></span>**WBEMMOF \_ \_ E-ALIASE \_ IN \_ EMBEDDED**
</dt> <dd> <dl> <dt>

2147762207 (0x8004401F)
</dt> <dt>



Eingebettete Objekte können keine Aliase sein.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_NULL_ARRAY_ELEM"></span><span id="wbemmof_e_null_array_elem"></span>**WBEMMOF \_ E \_ NULL \_ ARRAY \_ ELEM**
</dt> <dd> <dl> <dt>

2147762208 (0x80044020)
</dt> <dt>



NULL-Elemente in einem Array werden nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_DUPLICATE_QUALIFIER"></span><span id="wbemmof_e_duplicate_qualifier"></span>**WBEMMOF \_ E \_ DUPLICATE \_ QUALIFIER**
</dt> <dd> <dl> <dt>

2147762209 (0x80044021)
</dt> <dt>



Der Qualifizierer wurde für das Objekt mehr als einmal verwendet.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_FLAVOR_TYPE"></span><span id="wbemmof_e_expected_flavor_type"></span>**WBEMMOF \_ E \_ ERWARTETER \_ \_ VARIANTENTYP**
</dt> <dd> <dl> <dt>

2147762210 (0x80044022)
</dt> <dt>



Es wurde ein Variantentyp wie **ToInstance,** **ToSubClass,** **EnableOverride oder** **DisableOverride erwartet.**


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INCOMPATIBLE_FLAVOR_TYPES"></span><span id="wbemmof_e_incompatible_flavor_types"></span>**WBEMMOF \_ E \_ INCOMPATIBLE \_ FLAVOR \_ TYPES**
</dt> <dd> <dl> <dt>

2147762211 (0x80044023)
</dt> <dt>



Die Kombination **von EnableOverride** und **DisableOverride** für denselben Qualifizierer ist nicht rechtsblass.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_MULTIPLE_ALIASES"></span><span id="wbemmof_e_multiple_aliases"></span>**WBEMMOF \_ E \_ MEHRERE \_ ALIASE**
</dt> <dd> <dl> <dt>

2147762212 (0x80044024)
</dt> <dt>



Ein Alias kann nicht zweimal verwendet werden.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INCOMPATIBLE_FLAVOR_TYPES2"></span><span id="wbemmof_e_incompatible_flavor_types2"></span>**WBEMMOF \_ E \_ INCOMPATIBLE \_ FLAVOR \_ TYPES2**
</dt> <dd> <dl> <dt>

2147762213 (0x80044025)
</dt> <dt>



Das Kombinieren **von Restricted**, und **ToInstance** oder **ToSubClass** ist nicht legal.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_NO_ARRAYS_RETURNED"></span><span id="wbemmof_e_no_arrays_returned"></span>**WBEMMOF \_ E \_ NO \_ ARRAYS \_ RETURNED**
</dt> <dd> <dl> <dt>

2147762214 (0x80044026)
</dt> <dt>



Methoden können keine Arraywerte zurückgeben.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_MUST_BE_IN_OR_OUT"></span><span id="wbemmof_e_must_be_in_or_out"></span>**WBEMMOF \_ E MUSS IN ODER OUT \_ \_ \_ \_ \_ SEIN.**
</dt> <dd> <dl> <dt>

2147762215 (0x80044027)
</dt> <dt>



Argumente müssen einen **In- oder** **Out-Qualifizierer** haben.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_FLAGS_SYNTAX"></span><span id="wbemmof_e_invalid_flags_syntax"></span>**SYNTAX FÜR UNGÜLTIGE \_ \_ \_ FLAGS VON WBEMMOF E \_**
</dt> <dd> <dl> <dt>

2147762216 (0x80044028)
</dt> <dt>



Die Flags-Syntax ist ungültig.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_BRACE_OR_BAD_TYPE"></span><span id="wbemmof_e_expected_brace_or_bad_type"></span>**WBEMMOF \_ E ERWARTETE \_ \_ GESCHWEIFTE KLAMMER \_ ODER \_ \_ FEHLERHAFTER TYP**
</dt> <dd> <dl> <dt>

2147762217 (0x80044029)
</dt> <dt>



Die letzte geschweifte Klammer und das Semikolon für eine Klasse fehlen.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_UNSUPPORTED_CIMV22_QUAL_VALUE"></span><span id="wbemmof_e_unsupported_cimv22_qual_value"></span>**WBEMMOF \_ E \_ UNSUPPORTED \_ CIMV22 \_ QUAL \_ VALUE**
</dt> <dd> <dl> <dt>

2147762218 (0x8004402A)
</dt> <dt>



Ein CIM-Feature der Version 2.2 wird für einen Qualifiziererwert nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_UNSUPPORTED_CIMV22_DATA_TYPE"></span><span id="wbemmof_e_unsupported_cimv22_data_type"></span>**WBEMMOF \_ E \_ UNSUPPORTED CIMV22 DATA TYPE (NICHT UNTERSTÜTZTER \_ CIMV22-DATENTYP) \_ \_**
</dt> <dd> <dl> <dt>

2147762219 (0x8004402B)
</dt> <dt>



Der CIM-Datentyp 2.2 wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_DELETEINSTANCE_SYNTAX"></span><span id="wbemmof_e_invalid_deleteinstance_syntax"></span>**WBEMMOF \_ E \_ UNGÜLTIGE \_ DELETEINSTANCE-SYNTAX \_**
</dt> <dd> <dl> <dt>

2147762220 (0x8004402C)
</dt> <dt>



Die Syntax der Löschinstanz ist ungültig. Dies sollte `#pragma DeleteInstance("instancepath", FAIL|NOFAIL)`


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_QUALIFIER_SYNTAX"></span><span id="wbemmof_e_invalid_qualifier_syntax"></span>**WBEMMOF \_ E \_ UNGÜLTIGE \_ QUALIFIZIERERSYNTAX \_**
</dt> <dd> <dl> <dt>

2147762221 (0x8004402D)
</dt> <dt>



Die Qualifizierersyntax ist ungültig. Diese sollte `qualifiername:type=value,scope(class|instance), flavorname` lauten.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_QUALIFIER_USED_OUTSIDE_SCOPE"></span><span id="wbemmof_e_qualifier_used_outside_scope"></span>**AUßERHALB DES BEREICHS VERWENDETER WBEMMOF \_ \_ \_ \_ \_ E-QUALIFIZIERER**
</dt> <dd> <dl> <dt>

2147762222 (0x8004402E)
</dt> <dt>



Der Qualifizierer wird außerhalb seines Bereichs verwendet.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_ERROR_CREATING_TEMP_FILE"></span><span id="wbemmof_e_error_creating_temp_file"></span>**WBEMMOF E ERROR CREATING TEMP FILE (WBEMMOF \_ \_ \_ E-FEHLER BEIM ERSTELLEN \_ EINER \_ TEMPORÄREN DATEI)**
</dt> <dd> <dl> <dt>

2147762223 (0x8004402F)
</dt> <dt>



Fehler beim Erstellen einer temporären Datei. Die temporäre Datei ist eine Zwischenphase der MOF-Kompilierung.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_ERROR_INVALID_INCLUDE_FILE"></span><span id="wbemmof_e_error_invalid_include_file"></span>**WBEMMOF \_ E \_ ERROR \_ INVALID \_ INCLUDE \_ FILE**
</dt> <dd> <dl> <dt>

2147762224 (0x80044030)
</dt> <dt>



Eine Datei, die vom Präprozessorbefehl in der MOF enthalten [ \# ist,](-include.md) ist ungültig.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_DELETECLASS_SYNTAX"></span><span id="wbemmof_e_invalid_deleteclass_syntax"></span>**WBEMMOF \_ E \_ INVALID \_ DELETECLASS \_ SYNTAX**
</dt> <dd> <dl> <dt>

2147762225 (0x80044031)
</dt> <dt>



Die Syntax für die Präprozessorbefehle [ \# pragma deleteinstance](pragma-deleteinstance.md) oder [ \# pragma deleteclass](pragma-deleteclass.md) ist ungültig.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Header<br/>                   | <dl> <dt>WbemCli.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WbemCli.idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[WMI-Rückgabecodes](wmi-return-codes.md)
</dt> </dl>

 

