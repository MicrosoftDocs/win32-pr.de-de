---
title: Remotedesktopdienste WMI-Anbieterfehlercodes (Wbemcli.h)
description: Vom Remotedesktopdienste WMI-Anbieter zurückgegebene Fehler. Eine Liste anderer WMI-Fehler finden Sie unter WMI-Fehlerkonstanten.
ms.assetid: 1e68c41d-f321-4bc5-ba30-b69f5ba741eb
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- WBEM_E_FAILED
- WBEM_E_NOT_FOUND
- WBEM_E_PROVIDER_FAILURE
- WBEM_E_TYPE_MISMATCH
- WBEM_E_OUT_OF_MEMORY
- WBEM_E_INVALID_PARAMETER
- WBEM_E_NOT_AVAILABLE
- WBEM_E_NOT_SUPPORTED
- WBEM_E_INVALID_NAMESPACE
- WBEM_E_INVALID_OBJECT
- WBEM_E_INITIALIZATION_FAILURE
- WBEM_E_INVALID_OPERATION
- WBEM_E_INVALID_QUERY
- WBEM_E_INVALID_QUERY_TYPE
- WBEM_E_ALREADY_EXISTS
- WBEM_E_INVALID_SYNTAX
- WBEM_E_READ_ONLY
- WBEM_E_PROVIDER_NOT_CAPABLE
- WBEM_E_ILLEGAL_NULL
- WBEM_E_VALUE_OUT_OF_RANGE
- WBEM_E_INVALID_METHOD
- WBEM_E_INVALID_METHOD_PARAMETERS
- WBEM_E_INVALID_OBJECT_PATH
api_location:
- Wbemcli.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f02b2c1cc07bbe9431f2d0e64252258d76de9e6f06c0d7b756b3a5af4e42bff2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869670"
---
# <a name="remote-desktop-services-wmi-provider-error-codes"></a>fehlercodes für Remotedesktopdienste WMI-Anbieter

In der folgenden Liste sind die vom Remotedesktopdienste WMI-Anbieter zurückgegebenen WMI-Fehler aufgeführt. Eine Liste anderer WMI-Fehler finden Sie unter [**WMI-Fehlerkonstanten.**](/windows/desktop/WmiSdk/wmi-error-constants)

<dl> <dt>

<span id="WBEM_E_FAILED"></span><span id="wbem_e_failed"></span>**Fehler bei WBEM \_ E \_**
</dt> <dd> <dl> <dt>

2147749889 (0x80041001)
</dt> <dt>



Fehler beim Methodenaufruf.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NOT_FOUND"></span><span id="wbem_e_not_found"></span>**WBEM \_ E \_ NICHT \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

2147749890 (0x80041002)
</dt> <dt>



Das Objekt konnte nicht gefunden werden.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_FAILURE"></span><span id="wbem_e_provider_failure"></span>**\_FEHLER BEIM WBEM-E-ANBIETER \_ \_**
</dt> <dd> <dl> <dt>

2147749892 (0x80041004)
</dt> <dt>



Der Anbieter ist zu einem anderen Zeitpunkt als während der Initialisierung fehlgeschlagen.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_TYPE_MISMATCH"></span><span id="wbem_e_type_mismatch"></span>**WBEM \_ E \_ TYPE \_ MISMATCH**
</dt> <dd> <dl> <dt>

2147749893 (0x80041005)
</dt> <dt>



Ein Typkonflikt ist aufgetreten.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_OUT_OF_MEMORY"></span><span id="wbem_e_out_of_memory"></span>**WBEM \_ E NICHT GENÜGEND \_ \_ \_ ARBEITSSPEICHER**
</dt> <dd> <dl> <dt>

2147749894 (0x80041006)
</dt> <dt>



Für die Operation war nicht genügend Arbeitsspeicher verfügbar.


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



Die Ressource, i. d. R. ein Remoteserver, ist momentan nicht verfügbar.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NOT_SUPPORTED"></span><span id="wbem_e_not_supported"></span>**WBEM \_ E WIRD NICHT \_ \_ UNTERSTÜTZT**
</dt> <dd> <dl> <dt>

2147749900 (0x8004100C)
</dt> <dt>



Das Feature bzw. die Operation wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_NAMESPACE"></span><span id="wbem_e_invalid_namespace"></span>**WBEM \_ E \_ UNGÜLTIGER \_ NAMESPACE**
</dt> <dd> <dl> <dt>

2147749902 (0x8004100E)
</dt> <dt>



Der angegebene Namespace konnte nicht gefunden werden.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_OBJECT"></span><span id="wbem_e_invalid_object"></span>**WBEM \_ E \_ UNGÜLTIGES \_ OBJEKT**
</dt> <dd> <dl> <dt>

2147749903 (0x8004100F)
</dt> <dt>



Die angegebene Instanz ist ungültig.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INITIALIZATION_FAILURE"></span><span id="wbem_e_initialization_failure"></span>**FEHLER BEI DER WBEM \_ \_ E-INITIALISIERUNG \_**
</dt> <dd> <dl> <dt>

2147749908 (0x80041014)
</dt> <dt>



Ein Modul, z. B. ein Anbieter, konnte aus internen Gründen nicht initialisiert werden.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_OPERATION"></span><span id="wbem_e_invalid_operation"></span>**WBEM \_ E \_ UNGÜLTIGER \_ VORGANG**
</dt> <dd> <dl> <dt>

2147749910 (0x80041016)
</dt> <dt>



Die angeforderte Operation ist ungültig. Dieser Fehler betrifft i. A. ungültige Versuche, Klassen oder Eigenschaften zu löschen. Dieser Fehler wird zurückgegeben, wenn versucht wird, eine Serverüberschreibungseigenschaft über die Gruppenrichtliniensteuerung zu ändern.


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



In einem Put-Vorgang wurde das **Flag wbemChangeFlagCreateOnly** angegeben, aber die Instanz ist bereits vorhanden.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_SYNTAX"></span><span id="wbem_e_invalid_syntax"></span>**WBEM \_ E \_ UNGÜLTIGE \_ SYNTAX**
</dt> <dd> <dl> <dt>

2147749921 (0x80041021)
</dt> <dt>



Die Abfrage ist nicht syntaktisch gültig.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_READ_ONLY"></span><span id="wbem_e_read_only"></span>**WBEM \_ E \_ READ \_ ONLY**
</dt> <dd> <dl> <dt>

2147749923 (0x80041023)
</dt> <dt>



Die Eigenschaft, die Sie ändern möchten, ist schreibgeschützt.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_NOT_CAPABLE"></span><span id="wbem_e_provider_not_capable"></span>**WBEM \_ E PROVIDER NOT CAPABLE (WBEM-E-ANBIETER \_ NICHT IN DER \_ \_ LAGE)**
</dt> <dd> <dl> <dt>

2147749924 (0x80041024)
</dt> <dt>



Der Anbieter kann den angeforderten Vorgang nicht ausführen. Der Vorgang kann eine zu komplexe Abfrage, das Abrufen einer Instanz, das Erstellen einer Klasse, das Aktualisieren einer Klasse, das Löschen einer Klasse oder das Aufzählen einer Klasse umfassen.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_ILLEGAL_NULL"></span><span id="wbem_e_illegal_null"></span>**WBEM \_ E \_ ILLEGAL \_ NULL**
</dt> <dd> <dl> <dt>

2147749928 (0x80041028)
</dt> <dt>



Der Wert **Nothing** / **NULL** wurde für eine Eigenschaft angegeben, die nicht **Nothing** NULL sein darf, z. B. / eine Eigenschaft, die durch einen [**Schlüssel-,**](/windows/desktop/WmiSdk/key-qualifier) [**Indizierten-**](/windows/desktop/WmiSdk/optional-qualifiers)oder [**Not \_ NULL-Qualifizierer**](/windows/desktop/WmiSdk/optional-qualifiers) gekennzeichnet ist.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_VALUE_OUT_OF_RANGE"></span><span id="wbem_e_value_out_of_range"></span>**WBEM \_ \_ E-WERT \_ AUßERHALB \_ DES \_ BEREICHS**
</dt> <dd> <dl> <dt>

2147749931 (0x8004102B)
</dt> <dt>



Die Anforderung wurde mit einem Wert außerhalb des gültigen Bereichs vorgenommen bzw. ist mit dem Typ nicht kompatibel.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_METHOD"></span><span id="wbem_e_invalid_method"></span>**WBEM \_ E \_ UNGÜLTIGE \_ METHODE**
</dt> <dd> <dl> <dt>

2147749934 (0x8004102E)
</dt> <dt>



Der angeforderte Methode ist nicht verfügbar.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_METHOD_PARAMETERS"></span><span id="wbem_e_invalid_method_parameters"></span>**WBEM \_ E \_ UNGÜLTIGE \_ \_ METHODENPARAMETER**
</dt> <dd> <dl> <dt>

2147749935 (0x8004102F)
</dt> <dt>



Die für die Methode bereitgestellten Parameter sind ungültig.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_OBJECT_PATH"></span><span id="wbem_e_invalid_object_path"></span>**WBEM \_ E \_ UNGÜLTIGER \_ \_ OBJEKTPFAD**
</dt> <dd> <dl> <dt>

2147749946 (0x8004103A)
</dt> <dt>



Der angegebene Objektpfad war ungültig.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                       |
| Header<br/>                   | <dl> <dt>Wbemcli.h</dt> </dl> |



 

