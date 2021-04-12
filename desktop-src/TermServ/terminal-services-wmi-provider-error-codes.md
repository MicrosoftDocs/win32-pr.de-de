---
title: Remotedesktopdienste Fehlercodes des WMI-Anbieters (wbemcli. h)
description: Fehler, die vom Remotedesktopdienste WMI-Anbieter zurückgegeben werden. Eine Liste mit anderen WMI-Fehlern finden Sie unter WMI-Fehler Konstanten.
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
ms.openlocfilehash: 252015a5d80a1487033ad285ce3080f4d666f0c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518989"
---
# <a name="remote-desktop-services-wmi-provider-error-codes"></a>Fehlercodes für den WMI-Anbieter Remotedesktopdienste

In der folgenden Liste werden die WMI-Fehler aufgeführt, die vom Remotedesktopdienste WMI-Anbieter zurückgegeben werden. Eine Liste mit anderen WMI-Fehlern finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants).

<dl> <dt>

<span id="WBEM_E_FAILED"></span><span id="wbem_e_failed"></span>**WBEM \_ E \_ fehlgeschlagen**
</dt> <dd> <dl> <dt>

2147749889 (0x80041001)
</dt> <dt>



Der Methodenaufrufe ist fehlgeschlagen.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NOT_FOUND"></span><span id="wbem_e_not_found"></span>**WBEM \_ E \_ nicht \_ gefunden**
</dt> <dd> <dl> <dt>

2147749890 (0x80041002 angezeigt)
</dt> <dt>



Das Objekt konnte nicht gefunden werden.


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



Für die Operation war nicht genügend Arbeitsspeicher verfügbar.


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



Die Ressource, i. d. R. ein Remoteserver, ist momentan nicht verfügbar.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NOT_SUPPORTED"></span><span id="wbem_e_not_supported"></span>**WBEM \_ E \_ \_ wird nicht unterstützt.**
</dt> <dd> <dl> <dt>

2147749900 (0x8004100c)
</dt> <dt>



Das Feature bzw. die Operation wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_NAMESPACE"></span><span id="wbem_e_invalid_namespace"></span>**WBEM \_ E ( \_ ungültiger \_ Namespace)**
</dt> <dd> <dl> <dt>

2147749902 (0x8004100e)
</dt> <dt>



Der angegebene Namespace konnte nicht gefunden werden.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_OBJECT"></span><span id="wbem_e_invalid_object"></span>**ungültiges WBEM- \_ \_ \_ Objekt**
</dt> <dd> <dl> <dt>

2147749903 (0x8004100f)
</dt> <dt>



Die angegebene Instanz ist ungültig.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INITIALIZATION_FAILURE"></span><span id="wbem_e_initialization_failure"></span>**WBEM \_ E- \_ Initialisierungs \_ Fehler**
</dt> <dd> <dl> <dt>

2147749908 (0x80041014)
</dt> <dt>



Ein Modul, z. b. ein Anbieter, konnte aus internen Gründen nicht initialisiert werden.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_OPERATION"></span><span id="wbem_e_invalid_operation"></span>**\_Ungültiger WBEM E- \_ \_ Vorgang**
</dt> <dd> <dl> <dt>

2147749910 (0x80041016)
</dt> <dt>



Die angeforderte Operation ist ungültig. Dieser Fehler betrifft i. A. ungültige Versuche, Klassen oder Eigenschaften zu löschen. Dieser Fehler wird bei dem Versuch zurückgegeben, eine Server Überschreibungs Eigenschaft durch die Gruppenrichtlinien Steuerung zu ändern.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_QUERY"></span><span id="wbem_e_invalid_query"></span>**\_ungültige WBEM E- \_ \_ Abfrage**
</dt> <dd> <dl> <dt>

2147749911 (0x80041017)
</dt> <dt>



Die Abfrage war syntaktisch ungültig.


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

<span id="WBEM_E_INVALID_SYNTAX"></span><span id="wbem_e_invalid_syntax"></span>**\_ungültige WBEM E- \_ \_ Syntax**
</dt> <dd> <dl> <dt>

2147749921 (0x80041021)
</dt> <dt>



Die Abfrage ist nicht syntaktisch gültig.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_READ_ONLY"></span><span id="wbem_e_read_only"></span>**WBEM \_ E schreibgeschützt \_ \_**
</dt> <dd> <dl> <dt>

2147749923 (0x80041023)
</dt> <dt>



Die Eigenschaft, die Sie ändern möchten, ist schreibgeschützt.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_NOT_CAPABLE"></span><span id="wbem_e_provider_not_capable"></span>**WBEM \_ E \_ - \_ Anbieter \_ ist nicht fähig**
</dt> <dd> <dl> <dt>

2147749924 (0x80041024)
</dt> <dt>



Der Anbieter kann den angeforderten Vorgang nicht ausführen. Der Vorgang kann eine Abfrage enthalten, die zu komplex ist, eine Instanz abruft, eine Klasse erstellt, eine Klasse aktualisiert, eine Klasse löscht oder eine Klasse auflistet.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_ILLEGAL_NULL"></span><span id="wbem_e_illegal_null"></span>**WBEM \_ E \_ unzulässig \_ null**
</dt> <dd> <dl> <dt>

2147749928 (0x80041028)
</dt> <dt>



 / Für eine Eigenschaft, die nicht NULL sein darf, wurde der Wert Nothing **null** angegeben / , z. b. eine, die durch einen [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier), einen [**indizierten**](/windows/desktop/WmiSdk/optional-qualifiers)oder einen [**nicht- \_ null**](/windows/desktop/WmiSdk/optional-qualifiers) -Qualifizierer gekennzeichnet ist.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_VALUE_OUT_OF_RANGE"></span><span id="wbem_e_value_out_of_range"></span>**\_der Wert von WBEM E liegt \_ \_ außerhalb \_ des zulässigen \_ Bereichs.**
</dt> <dd> <dl> <dt>

2147749931 (0x8004102b)
</dt> <dt>



Die Anforderung wurde mit einem Wert außerhalb des gültigen Bereichs vorgenommen bzw. ist mit dem Typ nicht kompatibel.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_METHOD"></span><span id="wbem_e_invalid_method"></span>**\_ungültige WBEM E- \_ \_ Methode**
</dt> <dd> <dl> <dt>

2147749934 (0x8004102e)
</dt> <dt>



Der angeforderte Methode ist nicht verfügbar.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_METHOD_PARAMETERS"></span><span id="wbem_e_invalid_method_parameters"></span>**\_ \_ ungültige \_ Methoden \_ Parameter für WBEM E**
</dt> <dd> <dl> <dt>

2147749935 (0x8004102f)
</dt> <dt>



Die für die Methode bereitgestellten Parameter sind ungültig.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_OBJECT_PATH"></span><span id="wbem_e_invalid_object_path"></span>**WBEM \_ E ( \_ ungültiger \_ Objekt \_ Pfad)**
</dt> <dd> <dl> <dt>

2147749946 (0x8004103a)
</dt> <dt>



Der angegebene Objekt Pfad war ungültig.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                       |
| Header<br/>                   | <dl> <dt>Wbemcli. h</dt> </dl> |



 

