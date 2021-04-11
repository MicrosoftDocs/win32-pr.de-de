---
title: Compilerfehler
description: Liste der Fehlermeldungen, die während der Kompilierung der Kompilierung generiert wurden
ms.assetid: 492eacdd-6bd1-49df-9112-3765f6c05f34
keywords:
- Fehler-Mittell, Compilerfehler
topic_type:
- apiref
api_name:
- Compiler Errors
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b4bb2189e824f82cc9247abc68844068d083b2f0
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "104102482"
---
# <a name="compiler-errors"></a>Compilerfehler

Die folgenden Fehlermeldungen werden während der Mittell-Kompilierung generiert:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Rückgabecode</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="MIDL2000"></span><span id="midl2000"></span><dl> <dt><strong>MIDL2000</strong></dt> </dl></td>
<td><dl> <dt><span id="must_specify__c_ext_for_abstract_declarators"></span><span id="MUST_SPECIFY__C_EXT_FOR_ABSTRACT_DECLARATORS"></span>für abstrakte Deklaratoren muss/c_ext angegeben werden.</dt> <dd> Abstrakte Deklaratoren stellen eine Microsoft-Erweiterung für RPC dar und sind nicht in DCE RPC definiert. Wenn die Datei abstrakte Deklaratoren enthält, können Sie daher nicht mit dem Schalter <a href="-osf.md"><strong>/OSF</strong></a> kompilieren, der eine strikte DCE-Kompatibilität erzwingt. In der mittleren Version 3,0 und höher wird der Schalter <a href="-c-ext.md"><strong>/c_ext</strong></a> als Standardwert verwendet. mit dem Schalter " <strong>/OSF</strong> " wird der Schalter <strong>/c_ext</strong> deaktiviert. Weitere Informationen zu abstrakten Deklaratoren finden Sie <a href="/windows/desktop/Rpc/the-acf-body">im ACF-Text</a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2001"></span><span id="midl2001"></span><dl> <dt><strong>MIDL2001</strong></dt> </dl></td>
<td><dl> <dt><span id="instantiation_of_data_is_illegal__you_must_use__extern__or__static_"></span><span id="INSTANTIATION_OF_DATA_IS_ILLEGAL__YOU_MUST_USE__EXTERN__OR__STATIC_"></span>die Instanziierung von Daten ist unzulässig. Sie müssen &quot; extern &quot; oder &quot; static verwenden.&quot;</dt> <dd> Deklaration und Initialisierung in der IDL-Datei sind nicht mit DCE RPC kompatibel. Diese Funktion ist eine Microsoft-Erweiterung, die bei der Kompilierung im DCE-Kompatibilitätsmodus (<a href="-osf.md"><strong>/OSF</strong></a>) nicht verfügbar ist.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2002"></span><span id="midl2002"></span><dl> <dt><strong>MIDL2002</strong></dt> </dl></td>
<td><dl> <dt><span id="compiler_stack_overflow"></span><span id="COMPILER_STACK_OVERFLOW"></span>compilerstapel Überlauf</dt> <dd> Der Compiler hat bei der Verarbeitung der IDL-Datei nicht genügend Stapel Speicher. Dieses Problem kann auftreten, wenn der Compiler eine komplexe Deklaration oder einen Ausdruck verarbeitet. Vereinfachen Sie die komplexe Deklaration oder den Ausdruck, um das Problem zu beheben.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2003"></span><span id="midl2003"></span><dl> <dt><strong>MIDL2003</strong></dt> </dl></td>
<td><dl> <dt><span id="redefinition"></span><span id="REDEFINITION"></span>Neudefinition</dt> <dd> Diese Fehlermeldung kann unter den folgenden Umständen angezeigt werden: ein Typ wurde neu definiert. ein Prozedur Prototyp wurde neu definiert. ein Member einer Struktur oder Union desselben Namens ist bereits vorhanden. ein Parameter mit demselben Namen ist bereits im Prototyp vorhanden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2004"></span><span id="midl2004"></span><dl> <dt><strong>MIDL2004</strong></dt> </dl></td>
<td><dl> <dt><span id="_auto_handle__binding_will_be_used"></span><span id="_AUTO_HANDLE__BINDING_WILL_BE_USED"></span>[auto_handle] Bindung wird verwendet</dt> <dd> Es wurde kein behandlertyp als Standard behandlertyp definiert. Der Compiler geht davon aus, dass ein automatisches Handle als Bindungs Handle für die angegebene Prozedur verwendet wird.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2005"></span><span id="midl2005"></span><dl> <dt><strong>MIDL2005</strong></dt> </dl></td>
<td><dl> <dt><span id="out_of_memory"></span><span id="OUT_OF_MEMORY"></span>nicht genügend Arbeitsspeicher</dt> <dd> Der Compiler konnte während der Kompilierung nicht über genügend Arbeitsspeicher verfügen. Reduzieren Sie die Größe oder Komplexität der IDL-Datei, oder weisen Sie dem Prozess mehr Speicherplatz zu.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2006"></span><span id="midl2006"></span><dl> <dt><strong>MIDL2006</strong></dt> </dl></td>
<td><dl> <dt><span id="recursive_definition"></span><span id="RECURSIVE_DEFINITION"></span>rekursive Definition</dt> <dd> Eine Struktur oder Union wurde rekursiv definiert. Dieser Fehler kann auftreten, wenn eine Zeiger Spezifikation in einer Definition der Struktur einer Struktur fehlt.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2007"></span><span id="midl2007"></span><dl> <dt><strong>MIDL2007</strong></dt> </dl></td>
<td><dl> <dt><span id="import_ignored__file_already_imported"></span><span id="IMPORT_IGNORED__FILE_ALREADY_IMPORTED"></span>Import wird ignoriert. Datei wurde bereits importiert.</dt> <dd> Beim Importieren einer IDL-Datei handelt es sich um einen idempotenten Vorgang. Das einmalige einschließen hat keine Auswirkungen. Alle außer der erste Import Vorgang werden ignoriert.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2008"></span><span id="midl2008"></span><dl> <dt><strong>MIDL2008</strong></dt> </dl></td>
<td><dl> <dt><span id="sparse_enums_require__c_ext_or__ms_ext"></span><span id="SPARSE_ENUMS_REQUIRE__C_EXT_OR__MS_EXT"></span>sparse-Aufstände erfordern/c_ext oder/ms_ext</dt> <dd> Das Zuweisen von Werten zu Enumerationskonstanten ist mit DCE RPC nicht kompatibel. Wenn Sie die Microsoft-Erweiterungen in der Mitte verwenden möchten, die das Zuweisen von Werten zu Enumerationskonstanten zulassen, können Sie nicht mit dem Schalter <a href="-osf.md"><strong>/OSF</strong></a> kompilieren, der eine strikte DCE-Kompatibilität erzwingt. In den Mittelwert Versionen 3,0 und höher wird die <a href="-c-ext.md"><strong>/c_ext</strong></a> und <a href="-ms-ext.md"><strong>/ms_ext</strong></a> Switches als Standard verwendet. der Schalter <strong>/OSF</strong> deaktiviert diese Erweiterungs Schalter.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2009"></span><span id="midl2009"></span><dl> <dt><strong>MIDL2009</strong></dt> </dl></td>
<td><dl> <dt><span id="undefined_symbol"></span><span id="UNDEFINED_SYMBOL"></span>nicht definiertes Symbol</dt> <dd> Ein nicht definiertes Symbol wurde in einem Ausdruck verwendet. Dieser Fehler kann auftreten, wenn Sie einen nicht definierten Enumerationswert verwenden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2010"></span><span id="midl2010"></span><dl> <dt><strong>MIDL2010</strong></dt> </dl></td>
<td><dl> <dt><span id="type_used_in_ACF_file_not_defined_in_IDL_file"></span><span id="type_used_in_acf_file_not_defined_in_idl_file"></span><span id="TYPE_USED_IN_ACF_FILE_NOT_DEFINED_IN_IDL_FILE"></span>Typ, der in der in der IDL-Datei definierten ACF-Datei verwendet wird</dt> <dd> Es wird ein nicht definierter Typ verwendet.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2011"></span><span id="midl2011"></span><dl> <dt><strong>MIDL2011</strong></dt> </dl></td>
<td><dl> <dt><span id="unresolved_type_declaration"></span><span id="UNRESOLVED_TYPE_DECLARATION"></span>aufgelöste Typdeklaration</dt> <dd> Der im Feld zusätzliche Fehlerinformationen gemeldete Typ wurde an anderer Stelle in der IDL-Datei nicht definiert.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2012"></span><span id="midl2012"></span><dl> <dt><strong>MIDL2012</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_wide-character_constants_requires__ms_ext_or__c_ext"></span><span id="USE_OF_WIDE-CHARACTER_CONSTANTS_REQUIRES__MS_EXT_OR__C_EXT"></span>die Verwendung von breit Zeichen Konstanten erfordert/ms_ext oder/c_ext</dt> <dd> Breit Zeichen Konstanten sind eine Microsoft-Erweiterung für DCE IDL. Wenn Sie den Datentyp <a href="wchar-t.md"><strong>wchar_t</strong></a>verwenden möchten, können Sie nicht mit dem Schalter <a href="-osf.md"><strong>/OSF</strong></a> kompilieren, der die Standard Schalter <a href="-ms-ext.md"><strong>/ms_ext</strong></a> und <a href="-c-ext.md"><strong>/c_ext</strong></a>des mittleren Compilers überschreibt.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2013"></span><span id="midl2013"></span><dl> <dt><strong>MIDL2013</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_wide_character_strings_requires__ms_ext_or__c_ext"></span><span id="USE_OF_WIDE_CHARACTER_STRINGS_REQUIRES__MS_EXT_OR__C_EXT"></span>die Verwendung von Zeichen folgen mit breit Zeichen erfordert/ms_ext oder/c_ext</dt> <dd> Breit Zeichen-Zeichen folgen Konstanten sind eine Microsoft-Erweiterung für DCE IDL. Wenn Sie den Datentyp <a href="wchar-t.md"><strong>wchar_t</strong></a>verwenden möchten, können Sie nicht mit dem Schalter <a href="-osf.md"><strong>/OSF</strong></a> kompilieren, der die Standard Schalter <a href="-ms-ext.md"><strong>/ms_ext</strong></a> und <a href="-c-ext.md"><strong>/c_ext</strong></a>des mittleren Compilers überschreibt.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2014"></span><span id="midl2014"></span><dl> <dt><strong>MIDL2014</strong></dt> </dl></td>
<td><dl> <dt><span id="inconsistent_redefinition_of_type_wchar_t"></span><span id="INCONSISTENT_REDEFINITION_OF_TYPE_WCHAR_T"></span>inkonsistente Neudefinition des Typs wchar_t</dt> <dd> Der Typ <a href="wchar-t.md"><strong>wchar_t</strong></a> wurde als Typ neu definiert, der nicht dem Ganzzahl ohne Vorzeichen Short-DOS * entspricht.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2015"></span><span id="midl2015"></span><dl> <dt><strong>MIDL2015</strong></dt> </dl></td>
<td><dl> <dt><span id="importlib_not_found"></span><span id="IMPORTLIB_NOT_FOUND"></span>importlib nicht gefunden.</dt> <dd> Der Compiler konnte die von der [ <a href="importlib.md"><strong>importlib</strong></a>]-Direktive angegebene Typbibliothek nicht finden. Stellen Sie sicher, dass der Pfad und der Name der Bibliothek korrekt sind.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2016"></span><span id="midl2016"></span><dl> <dt><strong>MIDL2016</strong></dt> </dl></td>
<td><dl> <dt><span id="two_library_blocks"></span><span id="TWO_LIBRARY_BLOCKS"></span>zwei Bibliotheks Blöcke</dt> <dd> Zwei Bibliotheks Blöcke (auch mit unterschiedlichen Namen) in derselben Quelldatei sind unzulässig. Kombiniert alle Elemente in einem einzelnen Bibliotheks Block.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2017"></span><span id="midl2017"></span><dl> <dt><strong>MIDL2017</strong></dt> </dl></td>
<td><dl> <dt><span id="the_dispinterface_statement_requires_a_definition_for_IDispatch"></span><span id="the_dispinterface_statement_requires_a_definition_for_idispatch"></span><span id="THE_DISPINTERFACE_STATEMENT_REQUIRES_A_DEFINITION_FOR_IDISPATCH"></span>die dispinterface-Anweisung erfordert eine Definition für IDispatch.</dt> <dd> Dieser Fehler tritt im Allgemeinen auf, wenn die Dateien Stdole2 Typbibliothek. tlb oder oaidl. idl nicht importiert werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2018"></span><span id="midl2018"></span><dl> <dt><strong>MIDL2018</strong></dt> </dl></td>
<td><dl> <dt><span id="error_accessing_type_library"></span><span id="ERROR_ACCESSING_TYPE_LIBRARY"></span>Fehler beim Zugriff auf die Typbibliothek</dt> <dd> Der Compiler konnte die angegebene Typbibliothek nicht finden. Stellen Sie sicher, dass Sie den Pfad richtig angegeben haben.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2019"></span><span id="midl2019"></span><dl> <dt><strong>MIDL2019</strong></dt> </dl></td>
<td><dl> <dt><span id="error_accessing_type_info"></span><span id="ERROR_ACCESSING_TYPE_INFO"></span>Fehler beim Zugriff auf Typinformationen.</dt> <dd> Die importierte Typbibliothek ist beschädigt, ungültig oder nur teilweise konstruiert.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2020"></span><span id="midl2020"></span><dl> <dt><strong>MIDL2020</strong></dt> </dl></td>
<td><dl> <dt><span id="error_generating_type_library"></span><span id="ERROR_GENERATING_TYPE_LIBRARY"></span>Fehler beim Erzeugen der Typbibliothek.</dt> <dd> Die Typbibliothek konnte nicht generiert werden. Eine mögliche Ursache für diesen Fehler ist die Angabe eines Pfads zur IDL-Datei mit mehr als 126 Zeichen. Der Oleaut32.dll unterstützt keine Pfadnamen mit mehr als 126 Zeichen.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2021"></span><span id="midl2021"></span><dl> <dt><strong>MIDL2021</strong></dt> </dl></td>
<td><dl> <dt><span id="duplicate_id"></span><span id="DUPLICATE_ID"></span>doppelte ID</dt> <dd> Anwendungen verwenden die <a href="id.md"><strong>ID</strong></a> -Anweisung in IDL-Dateien, um eine DISPID für Element Funktionen anzugeben. Die Element Funktionen können entweder Eigenschaften oder Methoden von Schnittstellen oder dispinterfaces sein. Dieser Fehler gibt an, dass die IDL-Datei die gleiche Bezeichnernummer für zwei Methoden oder Eigenschaften angibt.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2022"></span><span id="midl2022"></span><dl> <dt><strong>MIDL2022</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_or_missing_value_for_entry_attribute"></span><span id="ILLEGAL_OR_MISSING_VALUE_FOR_ENTRY_ATTRIBUTE"></span>Ungültiger oder fehlender Wert für das Entry-Attribut.</dt> <dd> Das-Argument für das Entry-Attribut kann entweder eine Zeichenfolge sein, die einen benannten Einstiegspunkt angibt, oder eine Ordinalzahl, die den Einstiegspunkt definiert. Dieses Argument ist entweder nicht vorhanden oder enthält einen ungültigen Wert.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2023"></span><span id="midl2023"></span><dl> <dt><strong>MIDL2023</strong></dt> </dl></td>
<td><dl> <dt><span id="error_recovery_assumes"></span><span id="ERROR_RECOVERY_ASSUMES"></span>Fehler bei der Wiederherstellung</dt> <dd> Der mittlerer l-Compiler hat ungültige Zeichen in der IDL-Datei gefunden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2024"></span><span id="midl2024"></span><dl> <dt><strong>MIDL2024</strong></dt> </dl></td>
<td><dl> <dt><span id="error_recovery_discards"></span><span id="ERROR_RECOVERY_DISCARDS"></span>Fehler bei der Wiederherstellung</dt> <dd> Der mittlerer l-Compiler hat ungültige Zeichen in der IDL-Datei gefunden. Die ungültigen Zeichen werden ignoriert.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2025"></span><span id="midl2025"></span><dl> <dt><strong>MIDL2025</strong></dt> </dl></td>
<td><dl> <dt><span id="syntax_error"></span><span id="SYNTAX_ERROR"></span>Syntax Fehler</dt> <dd> Der Compiler hat einen Syntax Fehler in der angegebenen Zeile erkannt.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2026"></span><span id="midl2026"></span><dl> <dt><strong>MIDL2026</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_recover_from_earlier_syntax_errors__aborting_compilation"></span><span id="CANNOT_RECOVER_FROM_EARLIER_SYNTAX_ERRORS__ABORTING_COMPILATION"></span>kann nach früheren Syntax Fehlern nicht wieder hergestellt werden. Kompilierung wird abgebrochen</dt> <dd> Der mittlerer l-Compiler versucht automatisch, nach Syntax Fehlern wiederherzustellen, indem syntaktische Elemente hinzugefügt oder entfernt werden. Diese Meldung gibt an, dass der Compiler trotz dieser Wiederherstellungs Versuche zu viele Fehler erkannt hat. Korrigieren Sie die angegebenen Fehler, und kompilieren Sie Sie neu.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2027"></span><span id="midl2027"></span><dl> <dt><strong>MIDL2027</strong></dt> </dl></td>
<td><dl> <dt><span id="unknown_pragma_option"></span><span id="UNKNOWN_PRAGMA_OPTION"></span>Unbekanntes Pragma-Option</dt> <dd> Das angegebene C-Pragma wird in der mittleren l nicht unterstützt. Entfernen Sie das-Pragma aus der IDL-Datei.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2028"></span><span id="midl2028"></span><dl> <dt><strong>MIDL2028</strong></dt> </dl></td>
<td><dl> <dt><span id="feature_not_implemented"></span><span id="FEATURE_NOT_IMPLEMENTED"></span>Funktion nicht implementiert</dt> <dd> Die Mittelwert Funktion ist zwar Teil der Sprachdefinition, wird jedoch nicht in Microsoft RPC implementiert und wird vom Mittelwert Compiler nicht unterstützt. Beispielsweise sind die folgenden sprach Features nicht implementiert: Bitset, Pipe und der internationale Zeichentyp. Das nicht implementierte sprach Feature wird im Feld zusätzliche Fehlerinformationen in der Fehlermeldung angezeigt.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2029"></span><span id="midl2029"></span><dl> <dt><strong>MIDL2029</strong></dt> </dl></td>
<td><dl> <dt><span id="type_not_implemented"></span><span id="TYPE_NOT_IMPLEMENTED"></span>Typ nicht implementiert</dt> <dd> Der angegebene Datentyp, obwohl es sich nicht um ein gesetztes Mittel-Schlüsselwort handelt, ist in Microsoft RPC nicht implementiert.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2030"></span><span id="midl2030"></span><dl> <dt><strong>MIDL2030</strong></dt> </dl></td>
<td><dl> <dt><span id="non-pointer_used_in_a_dereference_operation"></span><span id="NON-POINTER_USED_IN_A_DEREFERENCE_OPERATION"></span>nicht-Zeiger, der in einem dereferenzierungsvorgang verwendet wird</dt> <dd> Ein Datentyp, bei dem es sich nicht um einen Zeiger handelt, wurde Zeiger Vorgängen zugeordnet. Sie können nicht über den angegebenen nicht-Zeiger auf das Objekt zugreifen.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2031"></span><span id="midl2031"></span><dl> <dt><strong>MIDL2031</strong></dt> </dl></td>
<td><dl> <dt><span id="expression_has_a_divide_by_zero"></span><span id="EXPRESSION_HAS_A_DIVIDE_BY_ZERO"></span>der Ausdruck weist eine Division durch Null auf.</dt> <dd> Der Konstante Ausdruck enthält eine Division durch 0 (null).<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2032"></span><span id="midl2032"></span><dl> <dt><strong>MIDL2032</strong></dt> </dl></td>
<td><dl> <dt><span id="expression_uses_incompatible_types"></span><span id="EXPRESSION_USES_INCOMPATIBLE_TYPES"></span>Ausdruck verwendet nicht kompatible Typen</dt> <dd> Die linke und die Rechte Seite des Operators in einem Ausdruck weisen nicht kompatible Typen auf.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2033"></span><span id="midl2033"></span><dl> <dt><strong>MIDL2033</strong></dt> </dl></td>
<td><dl> <dt><span id="nonarray_expression_uses_index_operator"></span><span id="NONARRAY_EXPRESSION_USES_INDEX_OPERATOR"></span>Ausdruck "Arrayform" verwendet Index Operator</dt> <dd> Der Ausdruck verwendet die Array Indizierungs Operation für ein Datenelement, das nicht vom Arraytyp ist.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2034"></span><span id="midl2034"></span><dl> <dt><strong>MIDL2034</strong></dt> </dl></td>
<td><dl> <dt><span id="left-hand_side_of_expression_does_not_evaluate_to_struct_union_enum"></span><span id="LEFT-HAND_SIDE_OF_EXPRESSION_DOES_NOT_EVALUATE_TO_STRUCT_UNION_ENUM"></span>die linke Seite des Ausdrucks wird nicht zu struct/Union/Enum ausgewertet.</dt> <dd> Der direkte oder indirekte Verweis Operator &quot; . &quot; oder wurde &quot; -> &quot; auf ein Datenobjekt angewendet, das keine Struktur, Union oder Enumeration ist. Mit dem angegebenen-Objekt können Sie keinen direkten oder indirekten Verweis abrufen.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2035"></span><span id="midl2035"></span><dl> <dt><strong>MIDL2035</strong></dt> </dl></td>
<td><dl> <dt><span id="constant_expression_expected"></span><span id="CONSTANT_EXPRESSION_EXPECTED"></span>konstanter Ausdruck erwartet</dt> <dd> Ein konstanter Ausdruck wurde in der Syntax erwartet. Beispielsweise ist für Array Begrenzungen ein konstanter Ausdruck erforderlich. Der Compiler gibt diese Fehlermeldung aus, wenn die Array Grenze mit einer Variablen oder einem nicht definierten Symbol definiert ist.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2036"></span><span id="midl2036"></span><dl> <dt><strong>MIDL2036</strong></dt> </dl></td>
<td><dl> <dt><span id="expression_cannot_be_evaluated_at_compile_time"></span><span id="EXPRESSION_CANNOT_BE_EVALUATED_AT_COMPILE_TIME"></span>der Ausdruck kann zur Kompilierzeit nicht ausgewertet werden.</dt> <dd> Der Compiler kann einen Ausdruck nicht zur Kompilierzeit auswerten.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2037"></span><span id="midl2037"></span><dl> <dt><strong>MIDL2037</strong></dt> </dl></td>
<td><dl> <dt><span id="expression_not_implemented"></span><span id="EXPRESSION_NOT_IMPLEMENTED"></span>Ausdruck nicht implementiert</dt> <dd> Eine Funktion, die in früheren Versionen des compl-Compilers unterstützt wurde, wird in der Version des mit Microsoft RPC bereitgestellten Compilers nicht unterstützt. Entfernen Sie den angegebenen Ausdruck.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2038"></span><span id="midl2038"></span><dl> <dt><strong>MIDL2038</strong></dt> </dl></td>
<td><dl> <dt><span id="no__pointer_default__attribute_specified__assuming__unique__for_all_unattributed_pointers"></span><span id="NO__POINTER_DEFAULT__ATTRIBUTE_SPECIFIED__ASSUMING__UNIQUE__FOR_ALL_UNATTRIBUTED_POINTERS"></span>Es wurde kein [Pointer_default]-Attribut angegeben, wobei für alle nicht attributierten Zeiger [Unique] angenommen wird.</dt> <dd> Der mittlerer l-Compiler bietet drei verschiedene Standardfälle für Zeiger, die keine Zeiger Attribute aufweisen. Funktionsparameter, die Zeiger der obersten Ebene sind, werden standardmäßig auf [<a href="ref.md"><strong>ref</strong></a>]-Zeiger fest. Zeiger, die in Strukturen eingebettet sind, und Zeiger auf andere Zeiger (keine Zeiger auf oberster Ebene), werden standardmäßig auf den vom [<a href="pointer-default.md"><strong>Pointer_default</strong></a>]-Attribut angegebenen Typ festgelegt. Wenn kein [<strong>Pointer_default</strong>]-Attribut angegeben wird, werden diese nicht auf oberster Ebene basierenden Zeiger standardmäßig auf eindeutige Zeiger zurückzuführen. Diese Fehlermeldung gibt den letzten Fall an: Es wurde kein [<strong>Pointer_default</strong>]-Attribut angegeben, und es gibt mindestens einen Zeiger, der nicht auf oberster Ebene ist, der als eindeutiger Zeiger behandelt wird. Weitere Informationen finden Sie unter <a href="/windows/desktop/Rpc/default-pointer-types">Standard Zeiger Typen</a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2039"></span><span id="midl2039"></span><dl> <dt><strong>MIDL2039</strong></dt> </dl></td>
<td><dl> <dt><span id="interface_is_not_automation_marshaling_conformant"></span><span id="INTERFACE_IS_NOT_AUTOMATION_MARSHALING_CONFORMANT"></span>Schnittstelle ist nicht automatisierungsmarshallingkonform</dt> <dd> Die-Schnittstelle erfüllt die Anforderungen für eine OLE-Automatisierungsschnittstelle nicht. Stellen Sie sicher, dass die Schnittstelle von <strong>IUnknown</strong> oder <strong>IDispatch</strong>abgeleitet ist.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2040"></span><span id="midl2040"></span><dl> <dt><strong>MIDL2040</strong></dt> </dl></td>
<td><dl> <dt><span id="_out__only_parameter_cannot_be_a_pointer_to_an_open_structure"></span><span id="_OUT__ONLY_PARAMETER_CANNOT_BE_A_POINTER_TO_AN_OPEN_STRUCTURE"></span>[out] nur der Parameter darf kein Zeiger auf eine offene Struktur sein.</dt> <dd> Ein [<a href="out-idl.md"><strong>out</strong></a>]-only-Parameter wurde als Zeiger auf eine-Struktur verwendet, die als offene Struktur bezeichnet wird, deren übertragener Bereich und Größe zur Laufzeit bestimmt werden. Der Serverstub weiß nicht, wie viel Speicherplatz für eine offene Struktur belegt werden muss. Verwenden Sie einen Zeiger auf einen Zeiger auf die offene Struktur, und stellen Sie sicher, dass die Serveranwendung ausreichend Speicherplatz für die Struktur bereitstellt.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2041"></span><span id="midl2041"></span><dl> <dt><strong>MIDL2041</strong></dt> </dl></td>
<td><dl> <dt><span id="_out__only_parameter_cannot_be_an_unsized_string"></span><span id="_OUT__ONLY_PARAMETER_CANNOT_BE_AN_UNSIZED_STRING"></span>[out] nur der Parameter darf keine Zeichenfolge ohne Größen Zeichen sein.</dt> <dd> Ein Array mit dem String-Attribut wurde als [<a href="out-idl.md"><strong>out</strong></a>]-only-Parameter ohne Größenangabe deklariert. Der Serverstub benötigt Größen Informationen, um Arbeitsspeicher für die Zeichenfolge zuzuweisen. Sie können das Zeichen folgen Attribut entfernen und das Attribut [<a href="size-is.md"><strong>size_is</strong></a>] hinzufügen, oder Sie können den Parameter in einen [<strong>in, out</strong>]-Parameter ändern.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2042"></span><span id="midl2042"></span><dl> <dt><strong>MIDL2042</strong></dt> </dl></td>
<td><dl> <dt><span id="_out__parameter_is_not_a_pointer"></span><span id="_OUT__PARAMETER_IS_NOT_A_POINTER"></span>[out] der Parameter ist kein Zeiger.</dt> <dd> Alle [<a href="out-idl.md"><strong>out</strong></a>]-Parameter müssen Zeiger sein, und zwar gemäß der "callby-Value"-Konvention der Programmiersprache C. Der [<strong>out</strong>] direktionale Parameter gibt an, dass der Server einen Wert an den Client überträgt. Mit der "callby-Value"-Konvention kann der Serverdaten nur dann an den Client übertragen, wenn das Funktions Argument ein Zeiger ist.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2043"></span><span id="midl2043"></span><dl> <dt><strong>MIDL2043</strong></dt> </dl></td>
<td><dl> <dt><span id="open_structure_cannot_be_a_parameter"></span><span id="OPEN_STRUCTURE_CANNOT_BE_A_PARAMETER"></span>Open Structure kann kein Parameter sein.</dt> <dd> Eine offene Struktur enthält ein konformes Array als letztes Element. Eine Struktur oder Union wird abgeschnitten, wenn das letzte Element der Struktur oder Union ein konformes Array ist.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2044"></span><span id="midl2044"></span><dl> <dt><strong>MIDL2044</strong></dt> </dl></td>
<td><dl> <dt><span id="_out__context_handle_generic_handle_must_be_specified_as_a_pointer_to_that_handle_type"></span><span id="_OUT__CONTEXT_HANDLE_GENERIC_HANDLE_MUST_BE_SPECIFIED_AS_A_POINTER_TO_THAT_HANDLE_TYPE"></span>[out] das Kontext Handle/generische Handle muss als Zeiger auf den betreffenden Handlertyp angegeben werden.</dt> <dd> Ein Kontext Handle-oder benutzerdefinierter handle-Parameter mit dem direktionalen [<a href="out-idl.md"><strong>out</strong></a>]-Attribut muss ein Zeiger auf einen Zeiger sein.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2045"></span><span id="midl2045"></span><dl> <dt><strong>MIDL2045</strong></dt> </dl></td>
<td><dl> <dt><span id="context_handle_must_not_derive_from_a_type_that_has_the__transmit_as__attribute"></span><span id="CONTEXT_HANDLE_MUST_NOT_DERIVE_FROM_A_TYPE_THAT_HAS_THE__TRANSMIT_AS__ATTRIBUTE"></span>das Kontext Handle darf nicht von einem Typ abgeleitet werden, der über das [Transmit_as]-Attribut verfügt.</dt> <dd> Kontext Handles müssen als Kontext Handle-Typen übertragen werden. Sie können nicht als andere Typen übertragen werden und können nicht von [transmit_is], [<strong>represent_as</strong>], [<strong>Wire_marshal</strong>] oder [<strong>user_marshal</strong>] abgeleitet werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2046"></span><span id="midl2046"></span><dl> <dt><strong>MIDL2046</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_specify_a_variable_number_of_arguments_to_a_remote_procedure"></span><span id="CANNOT_SPECIFY_A_VARIABLE_NUMBER_OF_ARGUMENTS_TO_A_REMOTE_PROCEDURE"></span>Es kann keine Variable Anzahl von Argumenten für eine Remote Prozedur angegeben werden.</dt> <dd> Remote Prozedur Aufrufe, die eine Variable Anzahl von Argumenten zum Zeitpunkt der Kompilierung angeben, sind nicht mit der DCE-RPC-Definition kompatibel. Es ist nicht möglich, eine Variable Anzahl von Argumenten in Microsoft RPC zu verwenden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2047"></span><span id="midl2047"></span><dl> <dt><strong>MIDL2047</strong></dt> </dl></td>
<td><dl> <dt><span id="named_parameter_cannot_be__void_"></span><span id="NAMED_PARAMETER_CANNOT_BE__VOID_"></span>der benannte Parameter darf nicht leer sein. &quot;&quot;</dt> <dd> Ein Parameter mit dem Basistyp <a href="void.md"><strong>void</strong></a> wird mit einem Namen angegeben.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2048"></span><span id="midl2048"></span><dl> <dt><strong>MIDL2048</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_derives_from__coclass__or__module_"></span><span id="PARAMETER_DERIVES_FROM__COCLASS__OR__MODULE_"></span>Parameter wird von &quot; Co-Klasse &quot; oder &quot; Modul abgeleitet&quot;</dt> <dd> Die <a href="coclass.md"><strong>Co-Klasse</strong></a> gibt ein Objekt der obersten Ebene an, das Schnittstellen und dispinterfaces enthält. Er kann nicht als Parameter übergeben werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2049"></span><span id="midl2049"></span><dl> <dt><strong>MIDL2049</strong></dt> </dl></td>
<td><dl> <dt><span id="only_the_first_parameter_can_be_a_binding_handle__you_must_specify_the__ms_ext_switch"></span><span id="ONLY_THE_FIRST_PARAMETER_CAN_BE_A_BINDING_HANDLE__YOU_MUST_SPECIFY_THE__MS_EXT_SWITCH"></span>nur der erste Parameter kann ein Bindungs Handle sein. Sie müssen den Schalter/ms_ext angeben.</dt> <dd> DCE RPC ermöglicht nur den ersten Parameter als Bindungs handle. Beim Kompilieren mit dem <a href="-osf.md"><strong>/OSF</strong></a> -Schalter wird der Standard <a href="-ms-ext.md"><strong>-/ms_ext</strong></a> Schalter deaktiviert, der mehrere handle-Parameter unterstützt und Parameter in der anderen Position als der am weitesten links gerichteten Parameter behandelt.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2050"></span><span id="midl2050"></span><dl> <dt><strong>MIDL2050</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_use__comm_status__on_both_a_parameter_and_a_return_type"></span><span id="CANNOT_USE__COMM_STATUS__ON_BOTH_A_PARAMETER_AND_A_RETURN_TYPE"></span>[comm_status] kann nicht für einen Parameter und einen Rückgabetyp verwendet werden.</dt> <dd> Sowohl die Prozedur als auch einer ihrer Parameter verfügen über das [<a href="comm-status.md"><strong>comm_status</strong></a>]-Attribut. Das [<strong>comm_status</strong>]-Attribut gibt an, dass jeweils nur ein Datenobjekt vom Typ " <a href="error-status-t.md"><strong>error_status_t</strong></a>" sein kann.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2051"></span><span id="midl2051"></span><dl> <dt><strong>MIDL2051</strong></dt> </dl></td>
<td><dl> <dt><span id="__local__attribute_on_a_procedure_requires__ms_ext"></span><span id="__LOCAL__ATTRIBUTE_ON_A_PROCEDURE_REQUIRES__MS_EXT"></span> [local]-Attribut für eine Prozedur erfordert/ms_ext</dt> <dd> Das [<a href="local.md"><strong>local</strong></a>]-Attribut ist eine Microsoft-Erweiterung für DCE IDL. Wenn Sie dieses Attribut für eine Funktion verwenden möchten, können Sie nicht mit dem Schalter <a href="-osf.md"><strong>/OSF</strong></a> kompilieren. Der <strong>/OSF</strong> -Schalter überschreibt die Standard Schalter/- <a href="-ms-ext.md"><strong>ms_ext</strong></a> und <a href="-c-ext.md"><strong>/c_ext</strong></a>des compl-Compilers.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2052"></span><span id="midl2052"></span><dl> <dt><strong>MIDL2052</strong></dt> </dl></td>
<td><dl> <dt><span id="property_attributes_may_only_be_used_with_procedures"></span><span id="PROPERTY_ATTRIBUTES_MAY_ONLY_BE_USED_WITH_PROCEDURES"></span>Eigenschafts Attribute können nur mit Prozeduren verwendet werden.</dt> <dd> Falsche Verwendung eines [<a href="propget.md"><strong>propget</strong></a>], [<a href="propput.md"><strong>PROPPUT</strong></a>] oder [<a href="propputref.md"><strong>PROPPUTREF</strong></a>]-Attributs. Stellen Sie sicher, dass Sie den Funktionsnamen der Eigenschaft ordnungsgemäß geschrieben haben und dass die Eigenschaft und die Funktion denselben Namen haben.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2053"></span><span id="midl2053"></span><dl> <dt><strong>MIDL2053</strong></dt> </dl></td>
<td><dl> <dt><span id="a_procedure_may_not_have_more_than_one_property_attribute"></span><span id="A_PROCEDURE_MAY_NOT_HAVE_MORE_THAN_ONE_PROPERTY_ATTRIBUTE"></span>eine Prozedur darf nicht mehr als ein Eigenschafts Attribut aufweisen.</dt> <dd> Höchstens eines der Attribute [<a href="propget.md"><strong>propget</strong></a>], [<a href="propput.md"><strong>PROPPUT</strong></a>] oder [<a href="propputref.md"><strong>PROPPUTREF</strong></a>] kann für eine Funktion angegeben werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2054"></span><span id="midl2054"></span><dl> <dt><strong>MIDL2054</strong></dt> </dl></td>
<td><dl> <dt><span id="the_procedure_has_an_illegal_combination_of_operation_attributes"></span><span id="THE_PROCEDURE_HAS_AN_ILLEGAL_COMBINATION_OF_OPERATION_ATTRIBUTES"></span>die Prozedur weist eine ungültige Kombination von Vorgangs Attributen auf.</dt> <dd> Bestimmte Attribute können nicht in Verbindung mit anderen Attributen verwendet werden. Überprüfen Sie die Syntax der Mittel l-Sprache auf genaue Anforderungen und Syntax der Attribute, die in diesem Verfahren verwendet werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2055"></span><span id="midl2055"></span><dl> <dt><strong>MIDL2055</strong></dt> </dl></td>
<td><dl> <dt><span id="field_deriving_from_a_conformant_array_must_be_the_last_member_of_the_structure"></span><span id="FIELD_DERIVING_FROM_A_CONFORMANT_ARRAY_MUST_BE_THE_LAST_MEMBER_OF_THE_STRUCTURE"></span>das Feld, das von einem konformen Array abgeleitet wird, muss das letzte Element der Struktur sein.</dt> <dd> Die-Struktur enthält ein konformes Array, das nicht das letzte Element in der-Struktur ist. Das konforme Array muss als letztes Structure-Element angezeigt werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2056"></span><span id="midl2056"></span><dl> <dt><strong>MIDL2056</strong></dt> </dl></td>
<td><dl> <dt><span id="duplicate__case__label"></span><span id="DUPLICATE__CASE__LABEL"></span>doppelte [Case]-Bezeichnung</dt> <dd> Es wurde eine doppelte Case-Bezeichnung angegeben. Die doppelte Bezeichnung wird angezeigt.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2057"></span><span id="midl2057"></span><dl> <dt><strong>MIDL2057</strong></dt> </dl></td>
<td><dl> <dt><span id="no__default__case_specified_for_discriminated_union"></span><span id="NO__DEFAULT__CASE_SPECIFIED_FOR_DISCRIMINATED_UNION"></span>kein [Standard]-Fall für Unterscheidungs-Union angegeben</dt> <dd> Eine Unterscheidungs-Union wurde ohne Standardfall angegeben.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2058"></span><span id="midl2058"></span><dl> <dt><strong>MIDL2058</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_expression_cannot_be_resolved"></span><span id="ATTRIBUTE_EXPRESSION_CANNOT_BE_RESOLVED"></span>der Attribut Ausdruck kann nicht aufgelöst werden.</dt> <dd> Der Ausdruck, der dem-Attribut zugeordnet ist, kann nicht aufgelöst werden. Dieser Fehler tritt normalerweise auf, wenn eine Variable, die im Ausdruck angezeigt wird, nicht definiert ist. Der Fehler kann z. b. auftreten, wenn die Variable <em>s</em> nicht definiert ist und vom Attribut [<a href="size-is.md"><strong>size_is</strong></a>] verwendet wird.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2059"></span><span id="midl2059"></span><dl> <dt><strong>MIDL2059</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_expression_must_be_of_integral_type__no_support_for_64-bit_expressions"></span><span id="ATTRIBUTE_EXPRESSION_MUST_BE_OF_INTEGRAL_TYPE__NO_SUPPORT_FOR_64-BIT_EXPRESSIONS"></span>der Attribut Ausdruck muss einen ganzzahligen Typ aufweisen, keine Unterstützung für 64-Bit-Ausdrücke.</dt> <dd> Die angegebene Attribut Variable oder der angegebene Ausdruck muss ein ganzzahliger Typ sein. Dieser Fehler tritt auf, wenn der Attribut Ausdruckstyp nicht in eine ganze Zahl aufgelöst wird.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2060"></span><span id="midl2060"></span><dl> <dt><strong>MIDL2060</strong></dt> </dl></td>
<td><dl> <dt><span id="_byte_count__requires__ms_ext"></span><span id="_BYTE_COUNT__REQUIRES__MS_EXT"></span>[byte_count] erfordert/ms_ext</dt> <dd> Das [<a href="byte-count.md"><strong>byte_count</strong></a>]-Attribut ist eine Microsoft-Erweiterung für DCE IDL. Um dieses Attribut zu verwenden, können Sie nicht mit dem Schalter <a href="-osf.md"><strong>/OSF</strong></a> kompilieren, der die Standard Schalter/- <a href="-ms-ext.md"><strong>ms_ext</strong></a> und <a href="-c-ext.md"><strong>/c_ext</strong></a>des compilercompilers überschreibt.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2061"></span><span id="midl2061"></span><dl> <dt><strong>MIDL2061</strong></dt> </dl></td>
<td><dl> <dt><span id="_byte_count__can_be_applied_only_to_out_parameters_of_pointer_type"></span><span id="_BYTE_COUNT__CAN_BE_APPLIED_ONLY_TO_OUT_PARAMETERS_OF_POINTER_TYPE"></span>[byte_count] kann nur auf Out-Parameter vom Zeigertyp angewendet werden.</dt> <dd> Das [<a href="byte-count.md"><strong>byte_count</strong></a>]-Attribut kann nur auf [<a href="out-idl.md"><strong>out</strong></a>]-Parameter angewendet werden, und alle [<strong>out</strong>]-Parameter müssen Zeiger Typen sein.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2062"></span><span id="midl2062"></span><dl> <dt><strong>MIDL2062</strong></dt> </dl></td>
<td><dl> <dt><span id="_byte_count__cannot_be_specified_on_a_pointer_to_a_conformant_array_or_structure"></span><span id="_BYTE_COUNT__CANNOT_BE_SPECIFIED_ON_A_POINTER_TO_A_CONFORMANT_ARRAY_OR_STRUCTURE"></span>[byte_count] kann nicht in einem Zeiger auf ein konformes Array oder eine konforme Struktur angegeben werden.</dt> <dd> Das [<a href="byte-count.md"><strong>byte_count</strong></a>]-Attribut kann nicht auf ein konformes Array oder eine konforme Struktur angewendet werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2063"></span><span id="midl2063"></span><dl> <dt><strong>MIDL2063</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_specifying_the_byte_count_is_not__in__only_or_byte_count_parameter_is_not__out__only"></span><span id="PARAMETER_SPECIFYING_THE_BYTE_COUNT_IS_NOT__IN__ONLY_OR_BYTE_COUNT_PARAMETER_IS_NOT__OUT__ONLY"></span>der Parameter, der die Byte Anzahl angibt, ist nicht [in], oder der Byte count-Parameter ist nicht [out].</dt> <dd> Der Wert, der [<a href="byte-count.md"><strong>byte_count</strong></a>] zugeordnet ist, muss vom Client an den Server übertragen werden. Dabei muss es sich um einen [<a href="in.md"><strong>in</strong></a>]-Parameter handeln. Der [<strong>byte_count</strong>]-Parameter muss kein [<strong>in, out</strong>]-Parameter sein.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2064"></span><span id="midl2064"></span><dl> <dt><strong>MIDL2064</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_specifying_the_byte_count_is_not_an_integral_type"></span><span id="PARAMETER_SPECIFYING_THE_BYTE_COUNT_IS_NOT_AN_INTEGRAL_TYPE"></span>der Parameter, der die Byte Anzahl angibt, ist kein integraler Typ.</dt> <dd> Der Wert, der der Byte Anzahl zugeordnet ist, muss der ganzzahlige Typ <a href="int.md"><strong>int</strong></a>, <a href="small.md"><strong>Small</strong></a>, <a href="short.md"><strong>Short</strong></a>oder <a href="long.md"><strong>Long</strong></a>sein.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2065"></span><span id="midl2065"></span><dl> <dt><strong>MIDL2065</strong></dt> </dl></td>
<td><dl> <dt><span id="_byte_count__cannot_be_specified_on_a_parameter_with_size_attributes"></span><span id="_BYTE_COUNT__CANNOT_BE_SPECIFIED_ON_A_PARAMETER_WITH_SIZE_ATTRIBUTES"></span>[byte_count] kann nicht für einen Parameter mit Größen Attributen angegeben werden.</dt> <dd> Das [<a href="byte-count.md"><strong>byte_count</strong></a>]-Attribut kann nicht mit anderen Größen Attributen wie [<a href="size-is.md"><strong>size_is</strong></a>] oder [<a href="length-is.md"><strong>length_is</strong></a>] verwendet werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2066"></span><span id="midl2066"></span><dl> <dt><strong>MIDL2066</strong></dt> </dl></td>
<td><dl> <dt><span id="_case__expression_is_not_constant"></span><span id="_CASE__EXPRESSION_IS_NOT_CONSTANT"></span>[Case]-Ausdruck ist nicht konstant.</dt> <dd> Der für die Case-Bezeichnung angegebene Ausdruck ist keine Konstante.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2067"></span><span id="midl2067"></span><dl> <dt><strong>MIDL2067</strong></dt> </dl></td>
<td><dl> <dt><span id="_case__expression_is_not_of_integral_type"></span><span id="_CASE__EXPRESSION_IS_NOT_OF_INTEGRAL_TYPE"></span>[Case] der Ausdruck ist kein ganzzahliger Typ.</dt> <dd> Der für die Case-Bezeichnung angegebene Ausdruck ist kein ganzzahliger Typ.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2068"></span><span id="midl2068"></span><dl> <dt><strong>MIDL2068</strong></dt> </dl></td>
<td><dl> <dt><span id="specifying__context_handle__on_a_type_other_than_void___requires__ms_ext"></span><span id="SPECIFYING__CONTEXT_HANDLE__ON_A_TYPE_OTHER_THAN_VOID___REQUIRES__MS_EXT"></span>das Angeben von [context_handle] für einen anderen Typ als void * erfordert/ms_ext</dt> <dd> Bei der DCE-RPC-Kompatibilität muss das Kontext Handle ein Zeiger vom Typ <strong>void *</strong>sein. Wenn Sie möchten, dass die Kontext Handles anderen Typen als <strong>void *</strong>zugeordnet werden, verwenden Sie nicht den Mittelwert-Compilerschalter <a href="-osf.md"><strong>/OSF</strong></a>, der den Standard Schalter <a href="-ms-ext.md"><strong>/ms_ext</strong></a>des Mittelwert Compilers überschreibt.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2069"></span><span id="midl2069"></span><dl> <dt><strong>MIDL2069</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_specify_more_than_one_parameter_with_each_of_comm_status_fault_status"></span><span id="CANNOT_SPECIFY_MORE_THAN_ONE_PARAMETER_WITH_EACH_OF_COMM_STATUS_FAULT_STATUS"></span>Es kann nicht mehr als ein Parameter angegeben werden, wobei jede comm_status/fault_status</dt> <dd> Eine Prozedur kann nur über einen Parameter mit dem [<a href="comm-status.md"><strong>comm_status</strong></a>]-Attribut verfügen. Es kann höchstens einen Parameter mit dem [<a href="fault-status.md"><strong>fault_status</strong></a>]-Attribut aufweisen.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2070"></span><span id="midl2070"></span><dl> <dt><strong>MIDL2070</strong></dt> </dl></td>
<td><dl> <dt><span id="comm_status_fault_status_parameter_must_be_an__out__only_pointer_parameter"></span><span id="COMM_STATUS_FAULT_STATUS_PARAMETER_MUST_BE_AN__OUT__ONLY_POINTER_PARAMETER"></span>der comm_status/fault_status Parameter muss ein [out] only-Zeiger Parameter sein.</dt> <dd> Die Fehlercode Typen [<a href="comm-status.md"><strong>comm_status</strong></a>] und [<a href="fault-status.md"><strong>fault_status</strong></a>] werden vom Server an den Client übertragen und müssen daher als [<a href="out-idl.md"><strong>out</strong></a>]-Parameter angegeben werden. Aufgrund der Einschränkungen in der Programmiersprache C müssen alle [<strong>out</strong>]-Parameter Zeiger sein.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2071"></span><span id="midl2071"></span><dl> <dt><strong>MIDL2071</strong></dt> </dl></td>
<td><dl> <dt><span id="endpoint_syntax_error"></span><span id="ENDPOINT_SYNTAX_ERROR"></span>Endpunkt Syntax Fehler</dt> <dd> Die Endpunkt Syntax ist falsch.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2072"></span><span id="midl2072"></span><dl> <dt><strong>MIDL2072</strong></dt> </dl></td>
<td><dl> <dt><span id="inapplicable_attribute"></span><span id="INAPPLICABLE_ATTRIBUTE"></span>nicht zutreffende Attribute</dt> <dd> Das angegebene Attribut kann nicht in diesem Konstrukt angewendet werden. Beispielsweise gilt das Zeichen folgen Attribut für <a href="char-idl.md"><strong>char</strong></a> -Arrays oder <strong>char</strong> -Zeiger und kann nicht auf eine-Struktur angewendet werden, die aus zwei <a href="short.md"><strong>kurzen</strong></a> Ganzzahlen besteht: <br/>
<pre class="syntax" data-space="preserve"><code>typedef [string] struct moo 
{
    short x;
    short y;
};</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2073"></span><span id="midl2073"></span><dl> <dt><strong>MIDL2073</strong></dt> </dl></td>
<td><dl> <dt><span id="_allocate__requires__ms_ext"></span><span id="_ALLOCATE__REQUIRES__MS_EXT"></span>[zuordnen] erfordert/ms_ext</dt> <dd> Das Attribut " <a href="allocate.md"><strong>zuordnen</strong></a> " stellt eine Microsoft-Erweiterung dar, die nicht als Teil von DCE RPC definiert ist. Wenn Sie dieses Attribut verwenden möchten, können Sie nicht mit dem Schalter <a href="-osf.md"><strong>/OSF</strong></a> kompilieren, der den Standard Schalter <a href="-ms-ext.md"><strong>/-ms_ext</strong></a> für den Mittelwert des Compilers überschreibt.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2074"></span><span id="midl2074"></span><dl> <dt><strong>MIDL2074</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid__allocate__mode"></span><span id="INVALID__ALLOCATE__MODE"></span>Ungültiger [zuordnen]-Modus</dt> <dd> Es wurde ein ungültiger Modus für das [<a href="allocate.md"><strong>zuordnen</strong></a>]-Attribut Konstrukt angegeben. Die vier gültigen Modi sind single_node, all_nodes, on_null und Always.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2075"></span><span id="midl2075"></span><dl> <dt><strong>MIDL2075</strong></dt> </dl></td>
<td><dl> <dt><span id="length_attributes_cannot_be_applied_with_string_attribute"></span><span id="LENGTH_ATTRIBUTES_CANNOT_BE_APPLIED_WITH_STRING_ATTRIBUTE"></span>Längen Attribute können nicht mit einem Zeichen folgen Attribut angewendet werden.</dt> <dd> Wenn das String-Attribut verwendet wird, <strong>wird die Zeichen</strong> folgen Länge von den generierten Stubdateien aufgerufen, um die Länge der Zeichenfolge zu bestimmen. Verwenden Sie für dieselbe Variable nicht das length-Attribut und das String-Attribut.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2076"></span><span id="midl2076"></span><dl> <dt><strong>MIDL2076</strong></dt> </dl></td>
<td><dl> <dt><span id="_last_is__and__length_is__cannot_be_specified_at_the_same_time"></span><span id="_LAST_IS__AND__LENGTH_IS__CANNOT_BE_SPECIFIED_AT_THE_SAME_TIME"></span>[Last_is] und [length_is] können nicht gleichzeitig angegeben werden.</dt> <dd> Für dasselbe Array wurden sowohl [<a href="last-is.md"><strong>Last_is</strong></a>] als auch [<a href="length-is.md"><strong>length_is</strong></a>] angegeben. Diese Attribute sind wie folgt verknüpft: length = Last First + 1. Da jeder Wert vom anderen abgeleitet werden kann, geben Sie nicht beides an.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2077"></span><span id="midl2077"></span><dl> <dt><strong>MIDL2077</strong></dt> </dl></td>
<td><dl> <dt><span id="_max_is__and__size_is__cannot_be_specified_at_the_same_time"></span><span id="_MAX_IS__AND__SIZE_IS__CANNOT_BE_SPECIFIED_AT_THE_SAME_TIME"></span>[Max_is] und [size_is] können nicht gleichzeitig angegeben werden.</dt> <dd> Für dasselbe Array wurden sowohl [ <a href="max-is.md"><strong>Max_is</strong></a>] als auch [ <a href="size-is.md"><strong>size_is</strong></a>] angegeben. Diese Attribute sind wie folgt verknüpft: max = size + 1. Da jeder Wert vom anderen abgeleitet werden kann, geben Sie nicht beides an.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2078"></span><span id="midl2078"></span><dl> <dt><strong>MIDL2078</strong></dt> </dl></td>
<td><dl> <dt><span id="no__switch_is__attribute_specified_at_use_of_union"></span><span id="NO__SWITCH_IS__ATTRIBUTE_SPECIFIED_AT_USE_OF_UNION"></span>kein [Switch_is]-Attribut für die Verwendung von Union angegeben.</dt> <dd> Für die Union wurde kein diskriminant angegeben. Das [<a href="switch-is.md"><strong>Switch_is</strong></a>]-Attribut gibt den Diskriminanten an, der zum Auswählen der Union-Felder verwendet wurde.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2079"></span><span id="midl2079"></span><dl> <dt><strong>MIDL2079</strong></dt> </dl></td>
<td><dl> <dt><span id="no__uuid__specified"></span><span id="NO__UUID__SPECIFIED"></span>No [UUID] angegeben</dt> <dd> Es wurde keine UUID für die Schnittstelle angegeben.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2080"></span><span id="midl2080"></span><dl> <dt><strong>MIDL2080</strong></dt> </dl></td>
<td><dl> <dt><span id="_uuid__ignored_on__local__interface"></span><span id="_UUID__IGNORED_ON__LOCAL__INTERFACE"></span>[UUID] wird auf [local]-Schnittstelle ignoriert.</dt> <dd> Das Verwenden des [<a href="local.md"><strong>local</strong></a>]-Attributs in einer Objektschnittstelle bewirkt, dass der Mittel l-Compiler das [<a href="uuid.md"><strong>UUID</strong></a>]-Attribut ignoriert. Beide Attribute können nicht für eine RPC-Schnittstelle verwendet werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2081"></span><span id="midl2081"></span><dl> <dt><strong>MIDL2081</strong></dt> </dl></td>
<td><dl> <dt><span id="type_mismatch_between_length_and_size_attribute_expressions"></span><span id="TYPE_MISMATCH_BETWEEN_LENGTH_AND_SIZE_ATTRIBUTE_EXPRESSIONS"></span>Typen Konflikt zwischen Attribut Ausdrücken für Länge und Größe</dt> <dd> Die Attribute "length" und "size" müssen denselben Typ aufweisen. Diese Warnung wird z. b. ausgegeben, wenn die Attribut Variable für den Ausdruck [<a href="size-is.md"><strong>size_is</strong></a>] den Typ <strong>Ganzzahl ohne Vorzeichen long</strong> hat und die Attribut Variable für den Ausdruck [<a href="length-is.md"><strong>length_is</strong></a>] den Typ <a href="long.md"><strong>Long</strong></a>hat.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2082"></span><span id="midl2082"></span><dl> <dt><strong>MIDL2082</strong></dt> </dl></td>
<td><dl> <dt><span id="_string__attribute_must_be_specified__byte____char___or__wchar_t__array_or_pointer"></span><span id="_STRING__ATTRIBUTE_MUST_BE_SPECIFIED__BYTE____CHAR___OR__WCHAR_T__ARRAY_OR_POINTER"></span>[String] das Attribut muss &quot; Byte, &quot; &quot; Char &quot; oder &quot; wchar_t &quot; Array oder Zeiger angegeben werden.</dt> <dd> Ein Zeichen folgen Attribut kann nicht auf einen Zeiger oder ein Array angewendet werden, dessen Basistyp kein <a href="byte.md"><strong>Byte</strong></a>, Zeichen oder <a href="struct.md"><strong>Struktur</strong></a> <a href="char-idl.md"><strong>ist, in</strong></a>dem die Elemente alle <strong>Byte</strong> -oder <strong>char</strong> -Typen sind.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2083"></span><span id="midl2083"></span><dl> <dt><strong>MIDL2083</strong></dt> </dl></td>
<td><dl> <dt><span id="mismatch_between_the_type_of_the__switch_is__expression_and_the_switch_type_of_the_union"></span><span id="MISMATCH_BETWEEN_THE_TYPE_OF_THE__SWITCH_IS__EXPRESSION_AND_THE_SWITCH_TYPE_OF_THE_UNION"></span>der Typ des [Switch_is]-Ausdrucks und der Switchtyp der Union stimmen nicht überein.</dt> <dd> Wenn die Union [<a href="switch-type.md"><strong>Switch_type</strong></a>] nicht angegeben wird, ist der Switchtyp derselbe Typ wie das Feld [<a href="switch-is.md"><strong>Switch_is</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2084"></span><span id="midl2084"></span><dl> <dt><strong>MIDL2084</strong></dt> </dl></td>
<td><dl> <dt><span id="_transmit_as__must_not_be_applied_to_a_type_that_derives_from_a_context_handle"></span><span id="_TRANSMIT_AS__MUST_NOT_BE_APPLIED_TO_A_TYPE_THAT_DERIVES_FROM_A_CONTEXT_HANDLE"></span>[Transmit_as] darf nicht auf einen Typ angewendet werden, der von einem Kontext Handle abgeleitet ist.</dt> <dd> Kontext Handles können nicht als andere Typen übertragen werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2085"></span><span id="midl2085"></span><dl> <dt><strong>MIDL2085</strong></dt> </dl></td>
<td><dl> <dt><span id="_transmit_as__must_specify_a_transmissible_type"></span><span id="_TRANSMIT_AS__MUST_SPECIFY_A_TRANSMISSIBLE_TYPE"></span>[Transmit_as] muss einen Transaktionstyp angeben.</dt> <dd> Der angegebene [<a href="transmit-as.md"><strong>Transmit_as</strong></a>]-Typ wird von einem Typ abgeleitet, der nicht von Microsoft RPC übertragen werden kann, z. b. <a href="void.md"><strong>void</strong></a>, <strong>void *</strong>oder <a href="int.md"><strong>int</strong></a>. Definierten RPC-Basistyp verwenden; Fügen Sie im Fall von <strong>int</strong>Größen Bearbeiter wie " <a href="small.md"><strong>Small</strong></a>", " <a href="short.md"><strong>Short</strong></a>" oder " <a href="long.md"><strong>Long</strong></a> " hinzu, um den <strong>int</strong>zu qualifizieren.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2086"></span><span id="midl2086"></span><dl> <dt><strong>MIDL2086</strong></dt> </dl></td>
<td><dl> <dt><span id="transmitted_type_for__transmit_as__and__represent_as__must_not_be_a_pointer_or_derive_from_a_pointer"></span><span id="TRANSMITTED_TYPE_FOR__TRANSMIT_AS__AND__REPRESENT_AS__MUST_NOT_BE_A_POINTER_OR_DERIVE_FROM_A_POINTER"></span>der übertragene Typ für [Transmit_as] und [represent_as] darf kein Zeiger sein oder von einem Zeiger abgeleitet werden.</dt> <dd> Der übertragene Typ kann kein Zeiger sein oder von einem Zeiger abgeleitet werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2087"></span><span id="midl2087"></span><dl> <dt><strong>MIDL2087</strong></dt> </dl></td>
<td><dl> <dt><span id="presented_type_for__transmit_as__and__represent_as__must_not_derive_from_a_conformant_varying_array__its_pointer_equivalent__or_a_conformant_varying_structure"></span><span id="PRESENTED_TYPE_FOR__TRANSMIT_AS__AND__REPRESENT_AS__MUST_NOT_DERIVE_FROM_A_CONFORMANT_VARYING_ARRAY__ITS_POINTER_EQUIVALENT__OR_A_CONFORMANT_VARYING_STRUCTURE"></span>der vorgestellte Typ für [Transmit_as] und [represent_as] darf nicht von einem konformen/variierenden Array, dessen Zeiger Entsprechung oder einer konformen/unterschiedlichen Struktur abgeleitet werden.</dt> <dd> Der Typ, auf den [<a href="transmit-as.md"><strong>Transmit_as</strong></a>] angewendet wurde, kann nicht von einem konformen Array oder einer Struktur abgeleitet werden (ein Array oder eine Struktur, deren Größe zur Laufzeit bestimmt wird).<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2088"></span><span id="midl2088"></span><dl> <dt><strong>MIDL2088</strong></dt> </dl></td>
<td><dl> <dt><span id="_uuid__format_is_incorrect"></span><span id="_UUID__FORMAT_IS_INCORRECT"></span>das Format [UUID] ist falsch.</dt> <dd> Das uuid-Format entspricht nicht der Spezifikation. Die UUID muss eine Zeichenfolge sein, die aus fünf Sequenz von hexadezimalen Ziffern der Länge 8, 4, 4, 4 und 12 Ziffern besteht. &quot;12345678-1234-ABCD-EF01-28a49c28f17d &quot; ist eine gültige UUID. Verwenden Sie die Funktion <a href="/windows/desktop/api/rpcdce/nf-rpcdce-uuidcreate"><strong>uuidcreate</strong></a> oder ein Hilfsprogramm, um eine gültige UUID zu generieren.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2089"></span><span id="midl2089"></span><dl> <dt><strong>MIDL2089</strong></dt> </dl></td>
<td><dl> <dt><span id="uuid_is_not_a_hexadecimal_number"></span><span id="UUID_IS_NOT_A_HEXADECIMAL_NUMBER"></span>UUID ist keine hexadezimal Zahl.</dt> <dd> Die für die Schnittstelle angegebene uuid enthält ungültige Zeichen in einer hexadezimalen Zahlen Darstellung. Die Zeichen 0 bis 9 und a bis F sind in einer hexadezimalen Darstellung gültig.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2090"></span><span id="midl2090"></span><dl> <dt><strong>MIDL2090</strong></dt> </dl></td>
<td><dl> <dt><span id="optional_parameters_must_come_after_required_parameters"></span><span id="OPTIONAL_PARAMETERS_MUST_COME_AFTER_REQUIRED_PARAMETERS"></span>optionale Parameter müssen nach den erforderlichen Parametern stehen.</dt> <dd> Eine Beschreibung der Reihenfolge von Parameterlisten finden Sie unter [<a href="optional.md"><strong>optional</strong></a>] in der Sprache der Mittel l-Sprache.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2091"></span><span id="midl2091"></span><dl> <dt><strong>MIDL2091</strong></dt> </dl></td>
<td><dl> <dt><span id="_dllname__required_when__entry__is_used"></span><span id="_DLLNAME__REQUIRED_WHEN__ENTRY__IS_USED"></span>[dllName] erforderlich, wenn [Entry] verwendet wird.</dt> <dd> Wenn Sie einen Einstiegspunkt in eine DLL-Datei angeben, müssen Sie auch den Namen der DLL angeben, indem Sie das [<a href="dllname-str-.md"><strong>dllName</strong></a>]-Attribut verwenden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2092"></span><span id="midl2092"></span><dl> <dt><strong>MIDL2092</strong></dt> </dl></td>
<td><dl> <dt><span id="_bindable__is_invalid_without__propget____propput___or__propputref_"></span><span id="_BINDABLE__IS_INVALID_WITHOUT__PROPGET____PROPPUT___OR__PROPPUTREF_"></span>[Bindable] ist ohne [Propget], [propput] oder [Propputref] ungültig.</dt> <dd> Das [<a href="bindable.md"><strong>bindbare</strong></a>]-Attribut ist nur für eine-Eigenschaft gültig. Daher müssen Sie auch eine der Funktionen zum Zugreifen auf Eigenschaften oder eine Eigenschaften Einstellung angeben.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2093"></span><span id="midl2093"></span><dl> <dt><strong>MIDL2093</strong></dt> </dl></td>
<td><dl> <dt><span id="procedures_with__propput__or__propputref__must_have_at_least_one_parameter"></span><span id="PROCEDURES_WITH__PROPPUT__OR__PROPPUTREF__MUST_HAVE_AT_LEAST_ONE_PARAMETER"></span>Prozeduren mit [propput] oder [Propputref] müssen mindestens einen Parameter aufweisen.</dt> <dd> Die Prozedur [<a href="propput.md"><strong>PROPPUT</strong></a>] oder [ <a href="propputref.md"><strong>PROPPUTREF</strong></a>] muss mindestens einen [<a href="in.md"><strong>in</strong></a>]-Parameter mit der festzulegenden-Eigenschaft aufweisen. eine [<a href="propget.md"><strong>propget</strong></a>]-Prozedur muss mindestens einen [<a href="out-idl.md"><strong>out</strong></a>, <a href="retval.md"><strong>retval</strong></a>]-Parameter aufweisen, um die Eigenschaft oder den Verweis zu empfangen.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2094"></span><span id="midl2094"></span><dl> <dt><strong>MIDL2094</strong></dt> </dl></td>
<td><dl> <dt><span id="_id__attribute_is_required"></span><span id="_ID__ATTRIBUTE_IS_REQUIRED"></span>[ID]-Attribut ist erforderlich.</dt> <dd> Diese Member-Funktion erfordert aufgrund der verwendeten <a href="dispinterface.md"><strong>dispinterface</strong></a> -Syntax eine DISPID, die Sie mithilfe des [ <a href="id.md"><strong>ID</strong></a>]-Attributs angeben. Wenn Sie mithilfe von Eigenschaften und Methoden eine <strong>dispinterface</strong> -Eigenschaft angeben, müssen Sie für jede Eigenschaft und Methode eine DISPID angeben.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2095"></span><span id="midl2095"></span><dl> <dt><strong>MIDL2095</strong></dt> </dl></td>
<td><dl> <dt><span id="interface_name_specified_in_the_ACF_does_not_match_that_specified_in_the_IDL_file"></span><span id="interface_name_specified_in_the_acf_does_not_match_that_specified_in_the_idl_file"></span><span id="INTERFACE_NAME_SPECIFIED_IN_THE_ACF_DOES_NOT_MATCH_THAT_SPECIFIED_IN_THE_IDL_FILE"></span>der in der ACF angegebene Schnittstellen Name stimmt nicht mit dem in der IDL-Datei angegebenen fest.</dt> <dd> Im aktuellen Compilermodus muss der Name, der auf das-Schnittstellen Schlüsselwort in der ACF folgt, mit dem Namen übereinstimmen, der auf das-Schnittstellen Schlüsselwort in der IDL-Datei folgt. Die Schnittstellennamen in den IDL-und ACF-Dateien können unterschiedlich sein, wenn Sie mit dem Mittell-Compilerschalter <a href="-acf.md"><strong>/ACF</strong></a>kompilieren.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2096"></span><span id="midl2096"></span><dl> <dt><strong>MIDL2096</strong></dt> </dl></td>
<td><dl> <dt><span id="duplicated_attribute"></span><span id="DUPLICATED_ATTRIBUTE"></span>doppeltes Attribut</dt> <dd> Doppelte oder widersprüchliche Attribute wurden angegeben. Dieser Fehler tritt häufig auf, wenn sich zwei Attribute gegenseitig ausschließen. Beispielsweise können die Attribute [<a href="code.md"><strong>Code</strong></a>] und [<a href="nocode.md"><strong>NoCode</strong></a>] nicht gleichzeitig verwendet werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2097"></span><span id="midl2097"></span><dl> <dt><strong>MIDL2097</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_with__comm_status__or__fault_status__attribute_must_be_a_pointer_to_type_error_status_t"></span><span id="PARAMETER_WITH__COMM_STATUS__OR__FAULT_STATUS__ATTRIBUTE_MUST_BE_A_POINTER_TO_TYPE_ERROR_STATUS_T"></span>der Parameter mit dem Attribut [comm_status] oder [fault_status] muss ein Zeiger auf den Typ sein error_status_t</dt> <dd> Wenn [<a href="fault-status.md"><strong>fault_status</strong></a>] oder [<a href="comm-status.md"><strong>comm_status</strong></a>] als Parameter Attribut verwendet wird, muss der Parameter ein [<a href="out-idl.md"><strong>out</strong></a>]-Parameter vom Typ <a href="error-status-t.md"><strong>error_status_t</strong></a>sein. Wenn ein Server Fehler auftritt, wird der-Parameter auf den Fehlercode festgelegt. Wenn der Remote-Befehl erfolgreich abgeschlossen wurde, legt die Prozedur den Wert fest.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2098"></span><span id="midl2098"></span><dl> <dt><strong>MIDL2098</strong></dt> </dl></td>
<td><dl> <dt><span id="a__local__procedure_cannot_be_specified_in_ACF_file"></span><span id="a__local__procedure_cannot_be_specified_in_acf_file"></span><span id="A__LOCAL__PROCEDURE_CANNOT_BE_SPECIFIED_IN_ACF_FILE"></span>eine [local]-Prozedur kann nicht in der ACF-Datei angegeben werden.</dt> <dd> Eine lokale Prozedur wurde in der ACF angegeben. Die lokale Prozedur kann nur in der IDL-Datei angegeben werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2099"></span><span id="midl2099"></span><dl> <dt><strong>MIDL2099</strong></dt> </dl></td>
<td><dl> <dt><span id="specified_type_is_not_defined_as_a_handle"></span><span id="SPECIFIED_TYPE_IS_NOT_DEFINED_AS_A_HANDLE"></span>der angegebene Typ ist nicht als handle definiert.</dt> <dd> Der im [<a href="implicit-handle.md"><strong>implicit_handle</strong></a>]-Attribut angegebene Typ ist nicht als handle-Typ definiert. Ändern Sie die Typdefinition oder den Typnamen, der vom-Attribut angegeben wird.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2100"></span><span id="midl2100"></span><dl> <dt><strong>MIDL2100</strong></dt> </dl></td>
<td><dl> <dt><span id="procedure_undefined"></span><span id="PROCEDURE_UNDEFINED"></span>Prozedur nicht definiert</dt> <dd> Ein Attribut wurde auf eine Prozedur in der ACF angewendet, und diese Prozedur ist nicht in der IDL-Datei definiert.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2101"></span><span id="midl2101"></span><dl> <dt><strong>MIDL2101</strong></dt> </dl></td>
<td><dl> <dt><span id="this_parameter_does_not_exist_in_the_IDL_file"></span><span id="this_parameter_does_not_exist_in_the_idl_file"></span><span id="THIS_PARAMETER_DOES_NOT_EXIST_IN_THE_IDL_FILE"></span>Dieser Parameter ist in der IDL-Datei nicht vorhanden.</dt> <dd> Ein in der ACF angegebener Parameter ist in der Definition in der IDL-Datei nicht vorhanden. Alle Parameter, Funktionen und Typdefinitionen, die in der ACF angezeigt werden, müssen den in der IDL-Datei zuvor definierten Parametern, Funktionen und Typen entsprechen.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2102"></span><span id="midl2102"></span><dl> <dt><strong>MIDL2102</strong></dt> </dl></td>
<td><dl> <dt><span id="this_array-bounds_construct_is_not_supported"></span><span id="THIS_ARRAY-BOUNDS_CONSTRUCT_IS_NOT_SUPPORTED"></span>Dieses Array-Begrenzungen-Konstrukt wird nicht unterstützt.</dt> <dd> Die Ober-und Untergrenze eines Arrays im formulararray [niedriger. Upper] nur, wenn die Konstante, die die untere Grenze des Arrays angibt, in den Wert 0 (null) aufgelöst wird.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2103"></span><span id="midl2103"></span><dl> <dt><strong>MIDL2103</strong></dt> </dl></td>
<td><dl> <dt><span id="array_bound_specification_is_illegal"></span><span id="ARRAY_BOUND_SPECIFICATION_IS_ILLEGAL"></span>die Array gebundene Spezifikation ist unzulässig.</dt> <dd> Die Benutzer Spezifikation der Array Begrenzungen für das Array mit fester Größe ist unzulässig. Beispiel: <br/>
<pre class="syntax" data-space="preserve"><code>typedef short Array[-1]</code></pre>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2104"></span><span id="midl2104"></span><dl> <dt><strong>MIDL2104</strong></dt> </dl></td>
<td><dl> <dt><span id="pointer_to_a_conformant_array_or_an_array_that_contains_a_conformant_array_is_not_supported"></span><span id="POINTER_TO_A_CONFORMANT_ARRAY_OR_AN_ARRAY_THAT_CONTAINS_A_CONFORMANT_ARRAY_IS_NOT_SUPPORTED"></span>Ein Zeiger auf ein konformes Array oder ein Array, das ein konformes Array enthält, wird nicht unterstützt.</dt> <dd> Ungültige Verwendung des konformen Arrays. Informationen zu Regeln, die konforme Arrays Regeln, finden Sie unter <a href="/windows/desktop/Rpc/arrays-and-rpc">Arrays und RPC</a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2105"></span><span id="midl2105"></span><dl> <dt><strong>MIDL2105</strong></dt> </dl></td>
<td><dl> <dt><span id="pointee_array_does_not_derive_any_size"></span><span id="POINTEE_ARRAY_DOES_NOT_DERIVE_ANY_SIZE"></span>pointee/Array leitet keine Größe ab.</dt> <dd> Ein konformes Array wurde ohne Größenangabe angegeben. Sie können die Größe mit dem Attribut [<a href="max-is.md"><strong>Max_is</strong></a>] oder [<a href="size-is.md"><strong>size_is</strong></a>] angeben.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2106"></span><span id="midl2106"></span><dl> <dt><strong>MIDL2106</strong></dt> </dl></td>
<td><dl> <dt><span id="only_fixed_arrays_and_SAFEARRAYs_are_legal_in_a_type_library"></span><span id="only_fixed_arrays_and_safearrays_are_legal_in_a_type_library"></span><span id="ONLY_FIXED_ARRAYS_AND_SAFEARRAYS_ARE_LEGAL_IN_A_TYPE_LIBRARY"></span>in einer Typbibliothek sind nur fixierte Arrays und SAFEARRAYs zulässig.</dt> <dd> Sie haben in einer Library-Anweisung einen Arraytyp verwendet, der nicht in einer Typbibliothek verwendet werden kann.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2107"></span><span id="midl2107"></span><dl> <dt><strong>MIDL2107</strong></dt> </dl></td>
<td><dl> <dt><span id="SAFEARRAYs_are_only_legal_inside_a_library_block"></span><span id="safearrays_are_only_legal_inside_a_library_block"></span><span id="SAFEARRAYS_ARE_ONLY_LEGAL_INSIDE_A_LIBRARY_BLOCK"></span>SAFEARRAYs sind nur innerhalb eines Bibliotheks Blocks zulässig.</dt> <dd> Der mittlerer l-Compiler erkennt ein SAFEARRAY nicht als gültigen Datentyp, es sei denn, es wird eine Typbibliothek erzeugt.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2108"></span><span id="midl2108"></span><dl> <dt><strong>MIDL2108</strong></dt> </dl></td>
<td><dl> <dt><span id="badly_formed_character_constant"></span><span id="BADLY_FORMED_CHARACTER_CONSTANT"></span>Ungültige Zeichen Konstante.</dt> <dd> Das Zeilenendezeichen ist in Zeichen Konstanten nicht zulässig.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2109"></span><span id="midl2109"></span><dl> <dt><strong>MIDL2109</strong></dt> </dl></td>
<td><dl> <dt><span id="end_of_file_found_in_comment"></span><span id="END_OF_FILE_FOUND_IN_COMMENT"></span>Dateiende in Kommentar gefunden</dt> <dd> Das Dateiendezeichen wurde in einem Kommentar gefunden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2110"></span><span id="midl2110"></span><dl> <dt><strong>MIDL2110</strong></dt> </dl></td>
<td><dl> <dt><span id="end_of_file_found_in_string"></span><span id="END_OF_FILE_FOUND_IN_STRING"></span>Dateiende in Zeichenfolge gefunden</dt> <dd> Das Dateiendezeichen ist in einer Zeichenfolge aufgetreten.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2111"></span><span id="midl2111"></span><dl> <dt><strong>MIDL2111</strong></dt> </dl></td>
<td><dl> <dt><span id="identifier_length_exceeds_31_characters"></span><span id="IDENTIFIER_LENGTH_EXCEEDS_31_CHARACTERS"></span>die Bezeichnerlänge überschreitet 31 Zeichen</dt> <dd> Bezeichner sind auf 31 alphanumerische Zeichen beschränkt. Bezeichnernamen, die länger als 31 Zeichen sind, werden abgeschnitten.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2112"></span><span id="midl2112"></span><dl> <dt><strong>MIDL2112</strong></dt> </dl></td>
<td><dl> <dt><span id="end_of_line_found_in_string"></span><span id="END_OF_LINE_FOUND_IN_STRING"></span>das Zeilenende wurde in der Zeichenfolge gefunden.</dt> <dd> Das Zeilenendezeichen wurde in der Zeichenfolge gefunden. Vergewissern Sie sich, dass Sie das doppelte Anführungszeichen eingeschlossen haben, das die Zeichenfolge beendet.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2113"></span><span id="midl2113"></span><dl> <dt><strong>MIDL2113</strong></dt> </dl></td>
<td><dl> <dt><span id="string_constant_exceeds_limit_of_255_characters"></span><span id="STRING_CONSTANT_EXCEEDS_LIMIT_OF_255_CHARACTERS"></span>die Zeichen folgen Konstante überschreitet das Limit von 255 Zeichen.</dt> <dd> Die Zeichenfolge hat die maximal zulässige Länge von 255 Zeichen überschritten.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2114"></span><span id="midl2114"></span><dl> <dt><strong>MIDL2114</strong></dt> </dl></td>
<td><dl> <dt><span id="identifier_exceeds_limit_of_255_characters_and_has_been_truncated"></span><span id="IDENTIFIER_EXCEEDS_LIMIT_OF_255_CHARACTERS_AND_HAS_BEEN_TRUNCATED"></span>der Bezeichner überschreitet das Limit von 255 Zeichen und wurde abgeschnitten.</dt> <dd> Der Bezeichner hat die maximal zulässige Länge von 255 Zeichen überschritten. Überschüssige Zeichen im Bezeichner werden abgeschnitten.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2115"></span><span id="midl2115"></span><dl> <dt><strong>MIDL2115</strong></dt> </dl></td>
<td><dl> <dt><span id="constant_too_big"></span><span id="CONSTANT_TOO_BIG"></span>Konstante zu groß</dt> <dd> Die Konstante ist zu groß, um intern dargestellt zu werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2116"></span><span id="midl2116"></span><dl> <dt><strong>MIDL2116</strong></dt> </dl></td>
<td><dl> <dt><span id="numerical_parsing_error"></span><span id="NUMERICAL_PARSING_ERROR"></span>numerischer Fehler bei der Verarbeitung</dt> <dd> Der Compiler konnte den numerischen Bezeichner nicht analysieren.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2117"></span><span id="midl2117"></span><dl> <dt><strong>MIDL2117</strong></dt> </dl></td>
<td><dl> <dt><span id="error_in_opening_file"></span><span id="ERROR_IN_OPENING_FILE"></span>Fehler beim Öffnen der Datei.</dt> <dd> Das Betriebssystem hat beim Versuch, eine Ausgabedatei zu öffnen, einen Fehler gemeldet. Dieser Fehler kann durch einen Namen verursacht werden, der für das Dateisystem zu lang ist, oder durch einen doppelten Dateinamen.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2118"></span><span id="midl2118"></span><dl> <dt><strong>MIDL2118</strong></dt> </dl></td>
<td>Fehler Bindung an Funktion<br/></td>
</tr>
<tr class="even">
<td><span id="MIDL2119"></span><span id="midl2119"></span><dl> <dt><strong>MIDL2119</strong></dt> </dl></td>
<td>Fehler beim Initialisieren von OLE.<br/></td>
</tr>
<tr class="odd">
<td><span id="MIDL2120"></span><span id="midl2120"></span><dl> <dt><strong>MIDL2120</strong></dt> </dl></td>
<td>Fehler beim Laden der Bibliothek<br/></td>
</tr>
<tr class="even">
<td><span id="MIDL2121"></span><span id="midl2121"></span><dl> <dt><strong>MIDL2121</strong></dt> </dl></td>
<td><dl> <dt><span id="_out__only_parameter_must_not_derive_from_a_top-level__unique__or__ptr__pointer_array"></span><span id="_OUT__ONLY_PARAMETER_MUST_NOT_DERIVE_FROM_A_TOP-LEVEL__UNIQUE__OR__PTR__POINTER_ARRAY"></span>[out] nur Parameter dürfen nicht von einem [Unique]-oder [PTR]-Zeiger/Array der obersten Ebene abgeleitet werden.</dt> <dd> Ein eindeutiger Zeiger darf kein [<a href="out-idl.md"><strong>out</strong></a>]-Parameter sein. Definitionsgemäß kann ein eindeutiger Zeiger von <strong>null</strong> in einen nicht-<strong>null</strong>-Wert geändert werden. Es werden keine Informationen über den [<strong>out</strong>]-Parameter vom Client an den Server übergeben.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2122"></span><span id="midl2122"></span><dl> <dt><strong>MIDL2122</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_is_not_applicable_to_this_non-rpcable_union"></span><span id="ATTRIBUTE_IS_NOT_APPLICABLE_TO_THIS_NON-RPCABLE_UNION"></span>das Attribut ist für diese nicht-rpcable-Union nicht anwendbar.</dt> <dd> Nur die Attribute [<a href="switch-is.md"><strong>Switch_is</strong></a>] und [<a href="switch-type.md"><strong>Switch_type</strong></a>] gelten für eine Union, die als Teil eines Remote Prozedur Aufrufes übertragen wird.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2123"></span><span id="midl2123"></span><dl> <dt><strong>MIDL2123</strong></dt> </dl></td>
<td><dl> <dt><span id="expression_used_for_a_size_attribute_must_not_derive_from_an__out_-only_parameter"></span><span id="EXPRESSION_USED_FOR_A_SIZE_ATTRIBUTE_MUST_NOT_DERIVE_FROM_AN__OUT_-ONLY_PARAMETER"></span>der für ein Size-Attribut verwendete Ausdruck darf nicht von einem [out]-Parameter abgeleitet werden.</dt> <dd> Der Wert eines [<a href="out-idl.md"><strong>out</strong></a>]-Parameters wird nicht an den Server übertragen und kann nicht verwendet werden, um die Länge oder Größe des [<a href="in.md"><strong>in</strong></a>]-Parameters zu bestimmen.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2124"></span><span id="midl2124"></span><dl> <dt><strong>MIDL2124</strong></dt> </dl></td>
<td><dl> <dt><span id="expression_used_for_a_length_attribute_for_an__in__parameter_cannot_derive_from_an__out_-only_parameter"></span><span id="EXPRESSION_USED_FOR_A_LENGTH_ATTRIBUTE_FOR_AN__IN__PARAMETER_CANNOT_DERIVE_FROM_AN__OUT_-ONLY_PARAMETER"></span>der Ausdruck, der für ein Längen Attribut für einen [in]-Parameter verwendet wird, kann nicht von einem [out]-Parameter abgeleitet werden.</dt> <dd> Der Wert eines [<a href="out-idl.md"><strong>out</strong></a>]-Parameters wird nicht an den Server übertragen und kann nicht verwendet werden, um die Länge oder Größe des [<a href="in.md"><strong>in</strong></a>]-Parameters zu bestimmen.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2125"></span><span id="midl2125"></span><dl> <dt><strong>MIDL2125</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of__int__needs__c_ext"></span><span id="USE_OF__INT__NEEDS__C_EXT"></span>Verwendung von &quot; int &quot; -Anforderungen/c_ext</dt> <dd> "Mittelwert" ist eine Sprache mit starker Typisierung. Alle über das Netzwerk übertragenen Parameter müssen von einem der mittleren Basis Typen abgeleitet werden. Der Typ " <a href="int.md"><strong>int</strong></a> " ist nicht als Teil von "Mittel l" definiert. Die übertragenen Daten müssen einen Größen Bezeichner enthalten: " <a href="small.md"><strong>Small</strong></a>", " <strong>Short</strong>" oder " <strong>Long</strong>". Daten, die nicht über das Netzwerk übertragen werden, können in eine Schnittstelle eingeschlossen werden. Verwenden Sie den Schalter <a href="-c-ext.md"><strong>/c_ext</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2126"></span><span id="midl2126"></span><dl> <dt><strong>MIDL2126</strong></dt> </dl></td>
<td><dl> <dt><span id="struct_union_field_must_not_be__void_"></span><span id="STRUCT_UNION_FIELD_MUST_NOT_BE__VOID_"></span>das Feld "Struct/Union" darf nicht leer sein. &quot;&quot;</dt> <dd> Felder in einer Struktur oder Union müssen als einen bestimmten Basistyp deklariert werden, der von der mittleren l unterstützt wird, oder einen Typ, der von den Basis Typen abgeleitet ist. Void-Typen sind in Remote Vorgängen nicht zulässig.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2127"></span><span id="midl2127"></span><dl> <dt><strong>MIDL2127</strong></dt> </dl></td>
<td><dl> <dt><span id="array_element_must_not_be_void"></span><span id="ARRAY_ELEMENT_MUST_NOT_BE_VOID"></span>Das Array Element darf nicht leer sein.</dt> <dd> Ein Array Element darf nicht leer sein.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2128"></span><span id="midl2128"></span><dl> <dt><strong>MIDL2128</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_type_qualifiers_and_or_modifiers_needs__c_ext"></span><span id="USE_OF_TYPE_QUALIFIERS_AND_OR_MODIFIERS_NEEDS__C_EXT"></span>Verwendung von typqualifizierern und/oder Modifizierern erfordert/c_ext</dt> <dd> Typmodifiziererer, z. b. <strong>_cdecl</strong> und <strong>_far</strong> , können nur kompiliert werden, wenn Sie den Schalter <a href="-c-ext.md"><strong>/c_ext</strong></a> angeben.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2129"></span><span id="midl2129"></span><dl> <dt><strong>MIDL2129</strong></dt> </dl></td>
<td><dl> <dt><span id="struct_union_field_must_not_derive_from_a_function"></span><span id="STRUCT_UNION_FIELD_MUST_NOT_DERIVE_FROM_A_FUNCTION"></span>das Feld "Struct/Union" darf nicht von einer Funktion abgeleitet werden.</dt> <dd> Die Felder einer Struktur oder Union müssen Mittel l-Basis Typen oder Typen sein, die von diesen Basis Typen abgeleitet werden. Funktionen sind in Struktur-oder Union-Feldern nicht zulässig.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2130"></span><span id="midl2130"></span><dl> <dt><strong>MIDL2130</strong></dt> </dl></td>
<td><dl> <dt><span id="array_element_must_not_be_a_function"></span><span id="ARRAY_ELEMENT_MUST_NOT_BE_A_FUNCTION"></span>Das Array Element darf keine Funktion sein.</dt> <dd> Ein Array Element kann keine Funktion sein.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2131"></span><span id="midl2131"></span><dl> <dt><strong>MIDL2131</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_must_not_be_a_function"></span><span id="PARAMETER_MUST_NOT_BE_A_FUNCTION"></span>der Parameter darf keine Funktion sein.</dt> <dd> Der Parameter für eine Remote Prozedur muss eine Variable eines angegebenen Typs sein. Eine Funktion kann kein Parameter für die Remote Prozedur sein.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2132"></span><span id="midl2132"></span><dl> <dt><strong>MIDL2132</strong></dt> </dl></td>
<td><dl> <dt><span id="struct_union_with_bit_fields_needs__c_ext"></span><span id="STRUCT_UNION_WITH_BIT_FIELDS_NEEDS__C_EXT"></span>Struktur/Union mit Bitfeldern muss/c_ext</dt> <dd> Sie müssen den Mittelwert-Compilerschalter <a href="-c-ext.md"><strong>/-c_ext</strong></a> angeben, um Bitfelder in Strukturen zuzulassen, die nicht in einem Remote Prozedur aufrufsvorgang übertragen werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2133"></span><span id="midl2133"></span><dl> <dt><strong>MIDL2133</strong></dt> </dl></td>
<td><dl> <dt><span id="bit_field_specification_on_a_type_other_that__int__is_a_non-ANSI-compatible_extension"></span><span id="bit_field_specification_on_a_type_other_that__int__is_a_non-ansi-compatible_extension"></span><span id="BIT_FIELD_SPECIFICATION_ON_A_TYPE_OTHER_THAT__INT__IS_A_NON-ANSI-COMPATIBLE_EXTENSION"></span>Bitfeld Spezifikation für einen Typ, der " &quot; int" &quot; eine nicht-ANSI-kompatible Erweiterung ist</dt> <dd> Die ANSI C-Programmiersprachen Spezifikation lässt nicht zu, dass Bitfelder auf nicht ganzzahlige Typen angewendet werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2134"></span><span id="midl2134"></span><dl> <dt><strong>MIDL2134</strong></dt> </dl></td>
<td><dl> <dt><span id="bit_field_specification_can_be_applied_only_to_simple__integral_types"></span><span id="BIT_FIELD_SPECIFICATION_CAN_BE_APPLIED_ONLY_TO_SIMPLE__INTEGRAL_TYPES"></span>die Bitfeld Spezifikation kann nur auf einfache, ganzzahlige Typen angewendet werden.</dt> <dd> Die ANSI C-Programmiersprachen Spezifikation lässt nicht zu, dass Bitfelder auf nicht ganzzahlige Typen angewendet werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2135"></span><span id="midl2135"></span><dl> <dt><strong>MIDL2135</strong></dt> </dl></td>
<td><dl> <dt><span id="struct_union_field_must_not_derive_from_handle_t_or_a_context-handle"></span><span id="STRUCT_UNION_FIELD_MUST_NOT_DERIVE_FROM_HANDLE_T_OR_A_CONTEXT-HANDLE"></span>das Feld "Struct/Union" darf nicht von handle_t oder einem Kontext Handle abgeleitet werden.</dt> <dd> Kontext Handles können nicht als Teil einer anderen Struktur übertragen werden. Sie müssen als Kontext Handles übertragen werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2136"></span><span id="midl2136"></span><dl> <dt><strong>MIDL2136</strong></dt> </dl></td>
<td><dl> <dt><span id="array_element_must_not_derive_from_handle_t_or_a_context_handle"></span><span id="ARRAY_ELEMENT_MUST_NOT_DERIVE_FROM_HANDLE_T_OR_A_CONTEXT_HANDLE"></span>Das Array Element darf nicht von handle_t oder einem Kontext Handle abgeleitet werden.</dt> <dd> Kontext Handles können nicht als Teil eines Arrays übertragen werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2137"></span><span id="midl2137"></span><dl> <dt><strong>MIDL2137</strong></dt> </dl></td>
<td><dl> <dt><span id="this_specification_of_union_needs__c_ext"></span><span id="THIS_SPECIFICATION_OF_UNION_NEEDS__C_EXT"></span>Diese Angabe von Union-Anforderungen/c_ext</dt> <dd> Eine Union, die in der Schnittstellen Definition angezeigt wird, muss dem Diskriminanten zugeordnet oder als lokal deklariert werden. Daten, die nicht über das Netzwerk übertragen werden, können implizit als Local deklariert werden, wenn Sie den <a href="-c-ext.md"><strong>/c_ext-</strong></a> Schalter verwenden, der die mittlere Standardeinstellung ist. Diese IDL kann nicht mit dem Schalter <a href="-osf.md"><strong>/OSF</strong></a> kompiliert werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2138"></span><span id="midl2138"></span><dl> <dt><strong>MIDL2138</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_deriving_from_an__int__must_have_size_specifier__small____short___or__long__with_the__int_"></span><span id="PARAMETER_DERIVING_FROM_AN__INT__MUST_HAVE_SIZE_SPECIFIER__SMALL____SHORT___OR__LONG__WITH_THE__INT_"></span>&quot;der Parameter, der von einem int abgeleitet &quot; &quot; wird, muss &quot; &quot; &quot; &quot; &quot; den &quot; Größen Bezeichner "Small", "Short" oder "Long" aufweisen&quot;</dt> <dd> Der Typ " <a href="int.md"><strong>int</strong></a> " ist nur ein gültiger Mittell-Typ auf 32-Bit-Plattformen, auf 16-Bit-Systemen <strong>int</strong> muss eine Größen Spezifikation sein. Verwenden Sie einen der größenspezifiken <a href="small.md"><strong>Small</strong></a>, <a href="short.md"><strong>Short</strong></a>oder <a href="long.md"><strong>Long</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2139"></span><span id="midl2139"></span><dl> <dt><strong>MIDL2139</strong></dt> </dl></td>
<td><dl> <dt><span id="type_of_the_parameter_cannot_derive_from_void_or_void_"></span><span id="TYPE_OF_THE_PARAMETER_CANNOT_DERIVE_FROM_VOID_OR_VOID_"></span>der Typ des Parameters kann nicht von void oder void abgeleitet werden *</dt> <dd> "Mittelwert" ist eine Sprache mit starker Typisierung. Alle über das Netzwerk übertragenen Parameter müssen von einem der mittleren Basis Typen abgeleitet werden. " <a href="void.md"><strong>Void</strong></a> " wird nicht als Basistyp unterstützt. Sie müssen die-Deklaration in einen gültigen Mittel l-Typ ändern.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2140"></span><span id="midl2140"></span><dl> <dt><strong>MIDL2140</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_deriving_from_a_struct_union_containing_bit_fields_is_not_supported"></span><span id="PARAMETER_DERIVING_FROM_A_STRUCT_UNION_CONTAINING_BIT_FIELDS_IS_NOT_SUPPORTED"></span>Parameter, die von einer Struktur/Union mit Bitfeldern abgeleitet werden, werden nicht unterstützt.</dt> <dd> Bitfelder werden von DCE RPC nicht als gültiger Datentyp definiert.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2141"></span><span id="midl2141"></span><dl> <dt><strong>MIDL2141</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_a_parameter_deriving_from_a_type_containing_type-modifiers_type-qualifiers_needs__c_ext"></span><span id="USE_OF_A_PARAMETER_DERIVING_FROM_A_TYPE_CONTAINING_TYPE-MODIFIERS_TYPE-QUALIFIERS_NEEDS__C_EXT"></span>Verwendung eines Parameters, der von einem Typ abgeleitet wird, der Typmodifizierer/typqualifiziereranforderungen/c_ext enthält</dt> <dd> Die Verwendung von Schlüsselwörtern wie " <strong>weit</strong>", " <strong>near</strong>", " <a href="const.md"><strong>konstant</strong></a>" und " <strong>volatile</strong> " in der IDL-Datei ist eine Microsoft-Erweiterung für DCE RPC. Diese Schlüsselwörter sind nicht verfügbar, wenn Sie mit dem <a href="-osf.md"><strong>/OSF</strong></a> -Schalter kompilieren, der den Standard <a href="-c-ext.md"><strong>-/c_ext</strong></a> Erweiterungs Schalter deaktiviert.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2142"></span><span id="midl2142"></span><dl> <dt><strong>MIDL2142</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_must_not_derive_from_a_pointer_to_a_function"></span><span id="PARAMETER_MUST_NOT_DERIVE_FROM_A_POINTER_TO_A_FUNCTION"></span>der Parameter darf nicht von einem Zeiger auf eine Funktion abgeleitet werden.</dt> <dd> Die RPC-Laufzeitbibliotheken übertragen einen Zeiger und die zugehörigen Daten zwischen Client und Server. Zeiger auf Funktionen können nicht als Parameter übertragen werden, da die Funktion nicht über das Netzwerk übertragen werden kann.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2143"></span><span id="midl2143"></span><dl> <dt><strong>MIDL2143</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_must_not_derive_from_a_nonrpccapable_union"></span><span id="PARAMETER_MUST_NOT_DERIVE_FROM_A_NONRPCCAPABLE_UNION"></span>der Parameter darf nicht von einer nicht-RPC-fähigen Union abgeleitet werden.</dt> <dd> Die Union muss mit einem Diskriminanten verknüpft werden. Verwenden Sie die Attribute [<a href="switch-is.md"><strong>Switch_is</strong></a>] und [<a href="switch-type.md"><strong>Switch_type</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2144"></span><span id="midl2144"></span><dl> <dt><strong>MIDL2144</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_derives_from_an__int.__You_must_use_size_specifiers_with_the__int_"></span><span id="return_type_derives_from_an__int.__you_must_use_size_specifiers_with_the__int_"></span><span id="RETURN_TYPE_DERIVES_FROM_AN__INT.__YOU_MUST_USE_SIZE_SPECIFIERS_WITH_THE__INT_"></span>der Rückgabetyp wird von einem &quot; int abgeleitet. &quot; Sie müssen größenspezifiken mit dem int-Typ verwenden. &quot;&quot;</dt> <dd> Bei 16-Bit-Systemen ist der Typ <a href="int.md"><strong>int</strong></a> kein gültiger Mittel l-Typ, es sei denn, er wird von einer Größenangabe begleitet. Verwenden Sie einen der größenspezifiken <a href="small.md"><strong>Small</strong></a>, <a href="short.md"><strong>Short</strong></a>oder <a href="long.md"><strong>Long</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2145"></span><span id="midl2145"></span><dl> <dt><strong>MIDL2145</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_must_not_derive_from_a_void_pointer"></span><span id="RETURN_TYPE_MUST_NOT_DERIVE_FROM_A_VOID_POINTER"></span>der Rückgabetyp darf nicht von einem void-Zeiger abgeleitet werden</dt> <dd> "Mittelwert" ist eine Sprache mit starker Typisierung. Alle über das Netzwerk übertragenen Parameter müssen von einem der mittleren Basis Typen abgeleitet werden. Void-Typen werden nicht als Teil von "Mittel l" definiert. Sie müssen die-Deklaration in einen gültigen Mittel l-Typ ändern.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2146"></span><span id="midl2146"></span><dl> <dt><strong>MIDL2146</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_must_not_derive_from_a_structure_union_containing_bit-fields"></span><span id="RETURN_TYPE_MUST_NOT_DERIVE_FROM_A_STRUCTURE_UNION_CONTAINING_BIT-FIELDS"></span>der Rückgabetyp darf nicht von einer Struktur/Union abgeleitet werden, die Bitfelder enthält.</dt> <dd> Bitfelder werden von DCE RPC nicht als gültiger Datentyp definiert.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2147"></span><span id="midl2147"></span><dl> <dt><strong>MIDL2147</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_must_not_derive_from_a_nonrpccapable_union"></span><span id="RETURN_TYPE_MUST_NOT_DERIVE_FROM_A_NONRPCCAPABLE_UNION"></span>Rückgabetyp darf nicht von einer nicht-RPC-fähigen Union abgeleitet werden</dt> <dd> Die Union muss mit einem Diskriminanten verknüpft werden. Verwenden Sie die Attribute [<a href="switch-is.md"><strong>Switch_is</strong></a>] und [<a href="switch-type.md"><strong>Switch_type</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2148"></span><span id="midl2148"></span><dl> <dt><strong>MIDL2148</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_must_not_derive_from_a_pointer_to_a_function"></span><span id="RETURN_TYPE_MUST_NOT_DERIVE_FROM_A_POINTER_TO_A_FUNCTION"></span>der Rückgabetyp darf nicht von einem Zeiger auf eine Funktion abgeleitet werden.</dt> <dd> Die RPC-Laufzeitbibliotheken übertragen einen Zeiger und die zugehörigen Daten zwischen Client und Server. Zeiger auf Funktionen können nicht als Parameter übertragen werden, da RPC keine Methode zum Übertragen der zugeordneten Funktion über das Netzwerk definiert.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2149"></span><span id="midl2149"></span><dl> <dt><strong>MIDL2149</strong></dt> </dl></td>
<td><dl> <dt><span id="compound_initializers_are_not_supported"></span><span id="COMPOUND_INITIALIZERS_ARE_NOT_SUPPORTED"></span>Verbund Initialisierer werden nicht unterstützt.</dt> <dd> DCE RPC unterstützt nur die einfache Initialisierung. Die Struktur oder das Array kann nicht in der IDL-Datei initialisiert werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2150"></span><span id="midl2150"></span><dl> <dt><strong>MIDL2150</strong></dt> </dl></td>
<td><dl> <dt><span id="ACF_attributes_in_the_IDL_file_need_the__app_config_switch"></span><span id="acf_attributes_in_the_idl_file_need_the__app_config_switch"></span><span id="ACF_ATTRIBUTES_IN_THE_IDL_FILE_NEED_THE__APP_CONFIG_SWITCH"></span>Für ACF-Attribute in der IDL-Datei ist der Schalter/app_config erforderlich.</dt> <dd> Eine Microsoft-Erweiterung ermöglicht Ihnen das Angeben von ACF-Attributen in der IDL-Datei. Verwenden Sie den Schalter <a href="-app-config.md"><strong>/app_config</strong></a> , um diese Erweiterung zu aktivieren.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2151"></span><span id="midl2151"></span><dl> <dt><strong>MIDL2151</strong></dt> </dl></td>
<td><dl> <dt><span id="single-line_comment_needs__ms_ext_or__c_ext"></span><span id="SINGLE-LINE_COMMENT_NEEDS__MS_EXT_OR__C_EXT"></span>einzeilige Kommentar Anforderungen/ms_ext oder/c_ext</dt> <dd> Einzeilige Kommentare, die zwei Schrägstriche (//) verwenden, stellen eine Microsoft-Erweiterung für DCE RPC dar. Sie können nur einzeilige Kommentare verwenden, wenn Sie mit dem <a href="-osf.md"><strong>/OSF</strong></a> -Schalter kompilieren.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2152"></span><span id="midl2152"></span><dl> <dt><strong>MIDL2152</strong></dt> </dl></td>
<td><dl> <dt><span id="_version__format_is_incorrect"></span><span id="_VERSION__FORMAT_IS_INCORRECT"></span>das Format [Version] ist falsch.</dt> <dd> Die Versionsnummer der-Schnittstelle im Schnittstellen Header muss im Format <em>Major</em>angegeben werden. <em>neben</em>Version, wobei jede Zahl zwischen 0 und 65535 liegen kann.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2153"></span><span id="midl2153"></span><dl> <dt><strong>MIDL2153</strong></dt> </dl></td>
<td><dl> <dt><span id="_signed__needs__ms_ext_or__c_ext"></span><span id="_SIGNED__NEEDS__MS_EXT_OR__C_EXT"></span>&quot;signierte &quot; Anforderungen/ms_ext oder/c_ext</dt> <dd> Die Verwendung des <a href="signed.md"><strong>signierten</strong></a> Schlüssel Worts ist eine Microsoft-Erweiterung für DCE RPC. Wenn Sie diese Funktion verwenden möchten, können Sie den Schalter <a href="-osf.md"><strong>/OSF</strong></a> nicht verwenden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2154"></span><span id="midl2154"></span><dl> <dt><strong>MIDL2154</strong></dt> </dl></td>
<td><dl> <dt><span id="mismatch_in_assignment_type"></span><span id="MISMATCH_IN_ASSIGNMENT_TYPE"></span>Konflikt beim Zuweisungstyp</dt> <dd> Der Typ der Variablen stimmt nicht mit dem Typ des Werts, der der Variablen zugewiesen ist, ab.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2155"></span><span id="midl2155"></span><dl> <dt><strong>MIDL2155</strong></dt> </dl></td>
<td><dl> <dt><span id="declaration_must_be_of_the_form__const__type__declarator_____initializing_expression_"></span><span id="DECLARATION_MUST_BE_OF_THE_FORM__CONST__TYPE__DECLARATOR_____INITIALIZING_EXPRESSION_"></span>die Deklaration muss folgendes Format aufweisen: konstant. <type><declarator> = <initializing expression></dt> <dd> Die-Deklaration ist nicht mit der DCE-RPC-Syntax kompatibel. Verwenden Sie den Schalter <a href="-ms-ext.md"><strong>/ms_ext</strong></a> oder <a href="-c-ext.md"><strong>/c_ext Mittel-</strong></a> Compilermodus.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2156"></span><span id="midl2156"></span><dl> <dt><strong>MIDL2156</strong></dt> </dl></td>
<td><dl> <dt><span id="declaration_must_have__const_"></span><span id="DECLARATION_MUST_HAVE__CONST_"></span>die Deklaration muss &quot; konstant sein.&quot;</dt> <dd> Deklarationen in der IDL-Datei müssen Konstante Ausdrücke sein, die das Schlüsselwort "Konstanten" verwenden, z. b <a href="const.md"><strong>.</strong></a>:<br/>
<pre class="syntax" data-space="preserve"><code>const short x = 2;</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2157"></span><span id="midl2157"></span><dl> <dt><strong>MIDL2157</strong></dt> </dl></td>
<td><dl> <dt><span id="struct_union_enum_must_not_be_defined_in_a_parameter-type_specification"></span><span id="STRUCT_UNION_ENUM_MUST_NOT_BE_DEFINED_IN_A_PARAMETER-TYPE_SPECIFICATION"></span>Struct/Union/Enum darf nicht in einer Parametertyp Spezifikation definiert werden.</dt> <dd> Der Struktur-, Union-oder enumerierte Typ muss explizit außerhalb des Funktions Prototyps angegeben werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2158"></span><span id="midl2158"></span><dl> <dt><strong>MIDL2158</strong></dt> </dl></td>
<td><dl> <dt><span id="_allocate__attribute_must_be_applied_only_on_non-void_pointer_types"></span><span id="_ALLOCATE__ATTRIBUTE_MUST_BE_APPLIED_ONLY_ON_NON-VOID_POINTER_TYPES"></span>[zuordnen] das Attribut muss nur für nicht-void-Zeiger Typen angewendet werden.</dt> <dd> Das Attribut [<a href="allocate.md"><strong>zuordnen</strong></a>] ist für komplexe Zeiger basierte Datenstrukturen konzipiert. Wenn das Attribut [zuordnen] angegeben ist, durchsucht die Stubdatei die Datenstruktur, um die Gesamtgröße aller Objekte zu berechnen, auf die vom Zeiger und allen anderen Zeigern in der Datenstruktur zugegriffen werden kann. Ändern Sie den Typ in einen nicht-void-Zeigertyp, oder entfernen Sie das<strong>Attribut [Allocation</strong>], und verwenden Sie eine andere Methode, <strong>um die</strong> zugehörige Zuordnungs Größe zu ermitteln, z. b.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2159"></span><span id="midl2159"></span><dl> <dt><strong>MIDL2159</strong></dt> </dl></td>
<td><dl> <dt><span id="array_or_equivalent_pointer_construct_cannot_derive_from_a_nonencapsulated_union"></span><span id="ARRAY_OR_EQUIVALENT_POINTER_CONSTRUCT_CANNOT_DERIVE_FROM_A_NONENCAPSULATED_UNION"></span>Array oder entsprechendes Zeiger Konstrukt können nicht von einer nicht gekapselten Union abgeleitet werden.</dt> <dd> Jede Union muss mit einem Diskriminanten verknüpft werden. Arrays von Unions sind nicht zulässig, da Sie den zugehörigen Diskriminanten nicht bereitstellen. Arrays von-Strukturen, in denen die-Struktur die Union und deren diskriminant verpackt, da die stufatoren den Diskriminanten zum Ermitteln der Größe der einzelnen Union verwenden können.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2160"></span><span id="midl2160"></span><dl> <dt><strong>MIDL2160</strong></dt> </dl></td>
<td><dl> <dt><span id="field_must_not_derive_from_an_error_status_t_type"></span><span id="FIELD_MUST_NOT_DERIVE_FROM_AN_ERROR_STATUS_T_TYPE"></span>das Feld darf nicht von einem error_status_t Typ abgeleitet werden.</dt> <dd> Der <a href="error-status-t.md"><strong>error_status_t</strong></a> -Typ kann nur als Parameter oder Rückgabetyp verwendet werden. Sie kann nicht in das Feld einer Struktur oder Union eingebettet werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2161"></span><span id="midl2161"></span><dl> <dt><strong>MIDL2161</strong></dt> </dl></td>
<td><dl> <dt><span id="union_has_at_least_one_arm_without_a_case_label"></span><span id="UNION_HAS_AT_LEAST_ONE_ARM_WITHOUT_A_CASE_LABEL"></span>Union weist mindestens einen Arm ohne Case-Bezeichnung auf.</dt> <dd> Die Union-Deklaration stimmt nicht mit der erforderlichen Mittel l-Syntax für die Union. Jeder Union-Arm erfordert eine Case-Bezeichnung oder eine Standard Bezeichnung, mit der dieser Union Arm ausgewählt wird.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2162"></span><span id="midl2162"></span><dl> <dt><strong>MIDL2162</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_or_return_value_must_not_derive_from_a_type_that_has__ignore__applied_to_it"></span><span id="PARAMETER_OR_RETURN_VALUE_MUST_NOT_DERIVE_FROM_A_TYPE_THAT_HAS__IGNORE__APPLIED_TO_IT"></span>der Parameter oder Rückgabewert darf nicht von einem Typ abgeleitet werden, auf den [Ignore] angewendet wurde.</dt> <dd> Das [<a href="ignore.md"><strong>Ignore</strong></a>]-Attribut ist ein Feld Attribut, das nur auf Felder angewendet werden kann, z. b. Felder von Strukturen und Arrays. Das [<strong>Ignore</strong>]-Attribut gibt an, dass der Stub den Zeiger während der Übertragung nicht dereferenzieren sollte und nicht zulässig ist, wenn er mit anderen Attributen in Konflikt steht, die dereferenziert werden müssen, z. b. [<a href="out-idl.md"><strong>out</strong></a>]-Parameter und Funktions Rückgabewerte.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2163"></span><span id="midl2163"></span><dl> <dt><strong>MIDL2163</strong></dt> </dl></td>
<td><dl> <dt><span id="pointer_already_has_a_pointer_attribute_applied_to_it"></span><span id="POINTER_ALREADY_HAS_A_POINTER_ATTRIBUTE_APPLIED_TO_IT"></span>auf den Zeiger wurde bereits ein Zeiger Attribut angewendet.</dt> <dd> Nur eines der Zeiger Attribute, [<a href="ref.md"><strong>ref</strong></a>], [<a href="unique.md"><strong>Unique</strong></a>] oder [<a href="ptr.md"><strong>ptr</strong></a>], kann auf einen einzelnen Zeiger angewendet werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2164"></span><span id="midl2164"></span><dl> <dt><strong>MIDL2164</strong></dt> </dl></td>
<td><dl> <dt><span id="field_parameter_must_not_derive_from_a_structure_that_is_recursive_through_a_ref_pointer"></span><span id="FIELD_PARAMETER_MUST_NOT_DERIVE_FROM_A_STRUCTURE_THAT_IS_RECURSIVE_THROUGH_A_REF_POINTER"></span>das Feld/der Parameter darf nicht von einer Struktur abgeleitet werden, die durch einen Verweis Zeiger rekursiv ist.</dt> <dd> Definitionsgemäß kann ein Verweis Zeiger nicht auf <strong>null</strong>festgelegt werden. Eine rekursive Datenstruktur, die mit einem Verweis Zeiger definiert ist, hat keine <strong>null</strong> -Elemente, und die Konvention wird nicht beendet. Verwenden Sie ein [<a href="unique.md"><strong>Unique</strong></a>]-Zeiger Attribut, damit die Datenstruktur ein <strong>null</strong> -Element angeben kann, oder definieren Sie die Datenstruktur als nicht rekursive Datenstruktur neu.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2165"></span><span id="midl2165"></span><dl> <dt><strong>MIDL2165</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_field_deriving_from_a_void_pointer_needs__c_ext"></span><span id="USE_OF_FIELD_DERIVING_FROM_A_VOID_POINTER_NEEDS__C_EXT"></span>Verwendung des Felds, das von einem void-Zeiger benötigt wird/c_ext</dt> <dd> Der Typ <strong>void *</strong> und andere Typen und Typqualifizierer, die nicht von DCE IDL unterstützt werden, sind nur in der IDL-Datei zulässig, wenn Sie die standardmäßigen Compilereinstellungen verwenden. Die Verwendung des <a href="-osf.md"><strong>/OSF</strong></a> -Schalters überschreibt diese Standardeinstellung. Wenn Sie im OSF-Kompatibilitätsmodus kompilieren müssen, müssen Sie den Zeigertyp neu definieren.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2166"></span><span id="midl2166"></span><dl> <dt><strong>MIDL2166</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_this_attribute_needs__ms_ext"></span><span id="USE_OF_THIS_ATTRIBUTE_NEEDS__MS_EXT"></span>Verwendung dieser Attribut Anforderungen/ms_ext</dt> <dd> Diese Sprachfunktion ist eine Microsoft-Erweiterung für DCE IDL. Diese Funktion kann nicht verwendet werden, wenn Sie im OSF-Kompatibilitätsmodus ( <a href="-osf.md"><strong>/OSF</strong></a> ) kompilieren.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2167"></span><span id="midl2167"></span><dl> <dt><strong>MIDL2167</strong></dt> </dl></td>
<td><dl> <dt><span id="this_attribute_only_allowed_with_new_format_type_libraries"></span><span id="THIS_ATTRIBUTE_ONLY_ALLOWED_WITH_NEW_FORMAT_TYPE_LIBRARIES"></span>Dieses Attribut ist nur mit neuen formattypbibliotheken zulässig.</dt> <dd> Um dieses Attribut zu verwenden, benötigen Sie die Version von Oleaut32.dll, die mit Windows 2000 oder höher bereitgestellt wird.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2168"></span><span id="midl2168"></span><dl> <dt><strong>MIDL2168</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_wchar_t_needs__ms_ext_or__c_ext"></span><span id="USE_OF_WCHAR_T_NEEDS__MS_EXT_OR__C_EXT"></span>Verwendung von wchar_t Anforderungen/ms_ext oder/c_ext</dt> <dd> Der breit Zeichentyp stellt eine Erweiterung für DCE-IDL dar. Der mittlerer l-Compiler akzeptiert den breit Zeichentyp nicht, wenn Sie den <a href="-osf.md"><strong>/OSF</strong></a> -Schalter angeben.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2169"></span><span id="midl2169"></span><dl> <dt><strong>MIDL2169</strong></dt> </dl></td>
<td><dl> <dt><span id="unnamed_fields_need__ms_ext_or__c_ext"></span><span id="UNNAMED_FIELDS_NEED__MS_EXT_OR__C_EXT"></span>unbenannte Felder benötigen/ms_ext oder/c_ext</dt> <dd> DCE IDL unterstützt nicht die Verwendung unbenannter Strukturen oder Unions, die in andere Strukturen oder Unions eingebettet sind. In DCE IDL müssen alle eingebetteten Felder benannt werden. Der mittlerer l-Compiler lässt seine Verwendung nicht zu, wenn Sie den <a href="-osf.md"><strong>/OSF</strong></a> -Schalter angeben.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2170"></span><span id="midl2170"></span><dl> <dt><strong>MIDL2170</strong></dt> </dl></td>
<td><dl> <dt><span id="unnamed_fields_can_derive_only_from_struct_union_types"></span><span id="UNNAMED_FIELDS_CAN_DERIVE_ONLY_FROM_STRUCT_UNION_TYPES"></span>unbenannte Felder können nur von Struktur-/Uniontypen abgeleitet werden.</dt> <dd> Die Microsoft-Erweiterung für die DCE-IDL, die unbenannte Felder unterstützt, gilt nur für Strukturen und Unions. Sie müssen dem Feld einen Namen zuweisen oder das Feld neu definieren, um diese Einschränkung einzuhalten.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2171"></span><span id="midl2171"></span><dl> <dt><strong>MIDL2171</strong></dt> </dl></td>
<td><dl> <dt><span id="field_of_a_union_cannot_derive_from_a_conformant_varying_array_or_its_pointer_equivalent"></span><span id="FIELD_OF_A_UNION_CANNOT_DERIVE_FROM_A_CONFORMANT_VARYING_ARRAY_OR_ITS_POINTER_EQUIVALENT"></span>das Feld einer Union kann nicht von einem konformen/variierenden Array oder seiner Zeiger Entsprechung abgeleitet werden.</dt> <dd> Das konforme Array darf in der Union nicht allein vorkommen, muss jedoch von dem Wert begleitet werden, der die Größe des Arrays angibt. Anstatt das Array als Union Arm zu verwenden, verwenden Sie eine Struktur, die aus dem konformen Array und dem Bezeichner besteht, der die Größe angibt.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2172"></span><span id="midl2172"></span><dl> <dt><strong>MIDL2172</strong></dt> </dl></td>
<td><dl> <dt><span id="no__pointer_default__attribute_specified__assuming__ptr__for_all_unattributed_pointers_in_interface"></span><span id="NO__POINTER_DEFAULT__ATTRIBUTE_SPECIFIED__ASSUMING__PTR__FOR_ALL_UNATTRIBUTED_POINTERS_IN_INTERFACE"></span>Es wurde kein [Pointer_default]-Attribut angegeben, vorausgesetzt [PTR] für alle nicht attributierten Zeiger in der Schnittstelle.</dt> <dd> Die DCE-IDL-Implementierung gibt an, dass alle Zeiger in jeder IDL-Dateizeiger Attributen zugeordnet werden müssen. Wenn ein explizites Zeiger Attribut nicht dem Parameter-oder Zeigertyp zugewiesen ist und kein [<a href="pointer-default.md"><strong>Pointer_default</strong></a>]-Attribut in der IDL-Datei angegeben ist, wird das vollständige Zeiger Attribut <a href="ptr.md"><strong>ptr</strong></a> dem Zeiger zugeordnet. Sie können die Zeiger Attribute mithilfe expliziter Zeiger Attribute ändern, indem Sie ein [<strong>Pointer_default</strong>]-Attribut angeben oder den <a href="-ms-ext.md"><strong>/ms_ext-</strong></a> Schalter angeben, um den Standardwert für nicht attributierte Zeiger auf [<a href="unique.md"><strong>Unique</strong></a>] zu ändern.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2173"></span><span id="midl2173"></span><dl> <dt><strong>MIDL2173</strong></dt> </dl></td>
<td><dl> <dt><span id="initializing_expression_must_resolve_to_a_constant_expression"></span><span id="INITIALIZING_EXPRESSION_MUST_RESOLVE_TO_A_CONSTANT_EXPRESSION"></span>Initialisieren des Ausdrucks muss in einen konstanten Ausdruck aufgelöst werden.</dt> <dd> Wenn ein Ausdruck als Initialisierer verwendet wird, muss der Ausdruck ein konstanter Ausdruck sein. Dies gilt für alle Mittel-compilermodi. Der Ausdruck muss zur Kompilierzeit auflösbar sein. Geben Sie eine Literalkonstante oder einen Ausdruck an, der zu einer Konstante und nicht zu einer Variablen aufgelöst wird.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2174"></span><span id="midl2174"></span><dl> <dt><strong>MIDL2174</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_expression_must_be_of_type_integer__char__Boolean_or_enum"></span><span id="attribute_expression_must_be_of_type_integer__char__boolean_or_enum"></span><span id="ATTRIBUTE_EXPRESSION_MUST_BE_OF_TYPE_INTEGER__CHAR__BOOLEAN_OR_ENUM"></span>der Attribut Ausdruck muss vom Typ Integer, Char, Boolean oder Enumeration sein.</dt> <dd> Der angegebene Typ wird nicht in einen gültigen Switchtyp aufgelöst. Verwenden Sie einen Integer-, Zeichen-, <a href="byte.md"><strong>Byte</strong></a>-, <a href="boolean.md"><strong>booleschen</strong></a>oder Enumerationstyp <a href="enum.md"><strong>oder einen Typ,</strong></a> der von einem dieser Typen abgeleitet ist.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2175"></span><span id="midl2175"></span><dl> <dt><strong>MIDL2175</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_constant"></span><span id="ILLEGAL_CONSTANT"></span>Ungültige Konstante</dt> <dd> Die angegebene Konstante liegt außerhalb des gültigen Bereichs für den angegebenen Typ.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2176"></span><span id="midl2176"></span><dl> <dt><strong>MIDL2176</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_not_implemented__ignored"></span><span id="ATTRIBUTE_NOT_IMPLEMENTED__IGNORED"></span>Attribut nicht implementiert; erten</dt> <dd> Das angegebene Attribut ist in dieser Version von Microsoft RPC nicht implementiert. Der-compilercompiler setzt die Verarbeitung der IDL-Datei fort, als wäre das Attribut nicht vorhanden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2177"></span><span id="midl2177"></span><dl> <dt><strong>MIDL2177</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_must_not_derive_from_a__ref__pointer"></span><span id="RETURN_TYPE_MUST_NOT_DERIVE_FROM_A__REF__POINTER"></span>der Rückgabetyp darf nicht von einem [REF]-Zeiger abgeleitet werden</dt> <dd> Funktions Rückgabewerte, die als Zeiger Typen definiert werden, müssen als [<a href="unique.md"><strong>Unique</strong></a>] oder <a href="ptr.md"><strong>vollständige</strong></a> Zeiger angegeben werden. Verweis Zeiger können nicht verwendet werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2178"></span><span id="midl2178"></span><dl> <dt><strong>MIDL2178</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_expression_must_be_a_variable_name_or_a_pointer_dereference_expression_in_this_mode._You_must_specify_the__ms_ext_switch"></span><span id="attribute_expression_must_be_a_variable_name_or_a_pointer_dereference_expression_in_this_mode._you_must_specify_the__ms_ext_switch"></span><span id="ATTRIBUTE_EXPRESSION_MUST_BE_A_VARIABLE_NAME_OR_A_POINTER_DEREFERENCE_EXPRESSION_IN_THIS_MODE._YOU_MUST_SPECIFY_THE__MS_EXT_SWITCH"></span>der Attribut Ausdruck muss ein Variablenname oder ein Zeiger dereferenzierungsausdruck in diesem Modus sein. Sie müssen den Schalter/ms_ext angeben.</dt> <dd> Der DCE-IDL-Compiler erfordert, dass die Größe, die dem [<a href="size-is.md"><strong>size_is</strong></a>]-Attribut zugeordnet ist, durch eine Variable oder eine Zeiger Variable angegeben wird. Wenn Sie die Microsoft-Erweiterung nutzen möchten, mit der das [<strong>size_is</strong>]-Attribut durch einen konstanten Ausdruck definiert werden kann, können Sie den <a href="-osf.md"><strong>/OSF</strong></a> -Compilerschalter nicht verwenden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2179"></span><span id="midl2179"></span><dl> <dt><strong>MIDL2179</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_must_not_derive_from_a_recursive_nonencapsulated_union"></span><span id="PARAMETER_MUST_NOT_DERIVE_FROM_A_RECURSIVE_NONENCAPSULATED_UNION"></span>der Parameter darf nicht von einer rekursiven nicht gekapselten Union abgeleitet werden</dt> <dd> Eine Union muss eine Diskriminante enthalten, sodass eine Union keine andere Union als Element aufweisen kann. Eine Union kann nur dann in eine andere Union eingebettet werden, wenn Sie Teil einer Struktur ist, die den Diskriminanten einschließt.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2180"></span><span id="midl2180"></span><dl> <dt><strong>MIDL2180</strong></dt> </dl></td>
<td><dl> <dt><span id="binding-handle_parameter_cannot_be__out__only"></span><span id="BINDING-HANDLE_PARAMETER_CANNOT_BE__OUT__ONLY"></span>der Bindungs handle-Parameter darf nicht [out] sein.</dt> <dd> Der vom Mittel l-Compiler als Bindungs Handle für diesen Vorgang identifizierte handle-Parameter muss ein [<a href="in.md"><strong>in</strong></a>]-Parameter sein. [<a href="out-idl.md"><strong>out</strong></a>]-nur Parameter sind im Clientstub nicht definiert, und das Bindungs Handle muss auf dem Client definiert werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2181"></span><span id="midl2181"></span><dl> <dt><strong>MIDL2181</strong></dt> </dl></td>
<td><dl> <dt><span id="pointer_to_a_handle_cannot_be__unique__or__ptr_"></span><span id="POINTER_TO_A_HANDLE_CANNOT_BE__UNIQUE__OR__PTR_"></span>Zeiger auf ein Handle darf nicht [eindeutig] oder [PTR] sein.</dt> <dd> Die Attribute Unique und Full Pointer können nicht für einen Zeiger auf ein Handle verwendet werden. Diese Attribute lassen den Wert <strong>null</strong>zu, und das Bindungs Handle darf nicht <strong>null</strong>sein. Verwenden Sie das [<a href="ref.md"><strong>ref</strong></a>]-Attribut, um den Bindungs handle-Parameter von Verweis Zeigern abzuleiten.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2182"></span><span id="midl2182"></span><dl> <dt><strong>MIDL2182</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_that_is_not_a_binding_handle_must_not_derive_from_handle_t"></span><span id="PARAMETER_THAT_IS_NOT_A_BINDING_HANDLE_MUST_NOT_DERIVE_FROM_HANDLE_T"></span>Parameter, der kein Bindungs Handle ist, darf nicht von abgeleitet werden handle_t</dt> <dd> Der primitive Handle-Typ <a href="handle-t.md"><strong>handle_t</strong></a> ist kein gültiger Datentyp, der über das Netzwerk übertragen wird. Ändern Sie den Parametertyp in einen anderen Typ als <strong>handle_t</strong>, oder entfernen Sie den Parameter.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2183"></span><span id="midl2183"></span><dl> <dt><strong>MIDL2183</strong></dt> </dl></td>
<td><dl> <dt><span id="unexpected_end_of_file_found"></span><span id="UNEXPECTED_END_OF_FILE_FOUND"></span>Unerwartetes Dateiende gefunden.</dt> <dd> Der mittlerer l-Compiler hat das Ende der Datei gefunden, bevor er alle syntaktischen Elemente der Datei erfolgreich auflösen konnte. Überprüfen Sie, ob am Ende der Datei das abschließende Recht geschweifter Klammer (}) vorhanden ist, oder überprüfen Sie die Syntax.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2184"></span><span id="midl2184"></span><dl> <dt><strong>MIDL2184</strong></dt> </dl></td>
<td><dl> <dt><span id="type_deriving_from_handle_t_must_not_have__transmit_as__applied_to_it"></span><span id="TYPE_DERIVING_FROM_HANDLE_T_MUST_NOT_HAVE__TRANSMIT_AS__APPLIED_TO_IT"></span>auf den Typ, der von handle_t abgeleitet ist, muss [Transmit_as] nicht angewendet werden.</dt> <dd> Der primitive Handle-Typ <a href="handle-t.md"><strong>handle_t</strong></a> wird nicht über das Netzwerk übertragen.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2185"></span><span id="midl2185"></span><dl> <dt><strong>MIDL2185</strong></dt> </dl></td>
<td><dl> <dt><span id="_context_handle__must_not_be_applied_to_a_type_that_has__handle__applied_to_it"></span><span id="_CONTEXT_HANDLE__MUST_NOT_BE_APPLIED_TO_A_TYPE_THAT_HAS__HANDLE__APPLIED_TO_IT"></span>[context_handle] darf nicht auf einen Typ angewendet werden, auf den [handle] angewendet wurde.</dt> <dd> Die Attribute [<a href="context-handle.md"><strong>context_handle</strong></a>] und [<a href="handle.md"><strong>handle</strong></a>] können nicht auf denselben Typ angewendet werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2186"></span><span id="midl2186"></span><dl> <dt><strong>MIDL2186</strong></dt> </dl></td>
<td><dl> <dt><span id="_handle__must_not_be_specified_on_a_type_deriving_from_void_or_void__"></span><span id="_HANDLE__MUST_NOT_BE_SPECIFIED_ON_A_TYPE_DERIVING_FROM_VOID_OR_VOID__"></span>[handle] darf nicht für einen Typ angegeben werden, der von "void" oder "void" abgeleitet ist *</dt> <dd> Ein mit dem Attribut [<a href="handle.md"><strong>handle</strong></a>] angegebener Typ kann über das Netzwerk übertragen werden, aber der Typ <strong>void *</strong> ist kein übertragbarer Typ. Der Handlertyp muss in einen Typ aufgelöst werden, der von den übertragbaren Basis Typen abgeleitet ist.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2187"></span><span id="midl2187"></span><dl> <dt><strong>MIDL2187</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_must_have_either__in____out__or__in_out__in_this_mode._You_must_specify__ms_ext_or__c_ext"></span><span id="parameter_must_have_either__in____out__or__in_out__in_this_mode._you_must_specify__ms_ext_or__c_ext"></span><span id="PARAMETER_MUST_HAVE_EITHER__IN____OUT__OR__IN_OUT__IN_THIS_MODE._YOU_MUST_SPECIFY__MS_EXT_OR__C_EXT"></span>der Parameter muss in diesem Modus entweder [in], [out] oder [in, out] aufweisen. Sie müssen/ms_ext oder/c_ext</dt> <dd> Der DCE-IDL-Compiler erfordert, dass alle Parameter explizite direktionale Parameter aufweisen. Wenn Sie die Microsoft-Erweiterungen für DCE IDL verwenden möchten, können Sie den Schalter <a href="-osf.md"><strong>/OSF</strong></a> nicht verwenden, der überschreibt <a href="-ms-ext.md"><strong>/ms_ext</strong></a> und <a href="-c-ext.md"><strong>/c_ext</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2188"></span><span id="midl2188"></span><dl> <dt><strong>MIDL2188</strong></dt> </dl></td>
<td><dl> <dt><span id="transmitted_type_may_not_derive_from__void__for__transmit_as____represent_as____wire_marshal____user_marshal_"></span><span id="TRANSMITTED_TYPE_MAY_NOT_DERIVE_FROM__VOID__FOR__TRANSMIT_AS____REPRESENT_AS____WIRE_MARSHAL____USER_MARSHAL_"></span>der übertragene Typ kann nicht von " &quot; void" &quot; für [Transmit_as], [represent_as], [Wire_marshal], [user_marshal] abgeleitet werden.</dt> <dd> Das [<a href="transmit-as.md"><strong>Transmit_as</strong></a>]-Attribut gilt nur für Zeiger Typen. Verwenden Sie den Typ <strong>void *</strong> anstelle von " <a href="void.md"><strong>void</strong></a>".<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2189"></span><span id="midl2189"></span><dl> <dt><strong>MIDL2189</strong></dt> </dl></td>
<td><dl> <dt><span id="_void__must_be_specified_on_the_first_and_only_parameter_specification"></span><span id="_VOID__MUST_BE_SPECIFIED_ON_THE_FIRST_AND_ONLY_PARAMETER_SPECIFICATION"></span>&quot;void &quot; muss in der ersten und einzigen Parameter Spezifikation angegeben werden.</dt> <dd> Das Schlüsselwort <a href="void.md"><strong>void</strong></a> wird fälschlicherweise mit anderen Funktionsparametern angezeigt. Um eine Funktion ohne Parameter anzugeben, muss das Schlüsselwort <strong>void</strong> das einzige Element der Parameterliste sein, wie im folgenden Beispiel gezeigt:<br/>
<pre class="syntax" data-space="preserve"><code>void Moo(void)</code></pre>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2190"></span><span id="midl2190"></span><dl> <dt><strong>MIDL2190</strong></dt> </dl></td>
<td><dl> <dt><span id="_switch_is__must_be_specified_only_on_a_type_deriving_from_a_nonencapsulated_union"></span><span id="_SWITCH_IS__MUST_BE_SPECIFIED_ONLY_ON_A_TYPE_DERIVING_FROM_A_NONENCAPSULATED_UNION"></span>[Switch_is] muss nur für einen Typ angegeben werden, der von einer nicht gekapselten Union abgeleitet ist.</dt> <dd> Das Schlüsselwort [<a href="switch-is.md"><strong>Switch_is</strong></a>] wurde falsch angewendet. Sie kann nur mit <a href="nonencapsulated-unions.md">nicht gekapselten Union-Typen</a>verwendet werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2191"></span><span id="midl2191"></span><dl> <dt><strong>MIDL2191</strong></dt> </dl></td>
<td><dl> <dt><span id="stringable_structures_are_not_implemented_in_this_version"></span><span id="STRINGABLE_STRUCTURES_ARE_NOT_IMPLEMENTED_IN_THIS_VERSION"></span>stringable-Strukturen sind in dieser Version nicht implementiert.</dt> <dd> DCE IDL ermöglicht das Anwenden des Attributs [<a href="string.md"><strong>String</strong></a>] auf eine Struktur, deren Elemente nur aus Zeichen, Bytes oder Typen bestehen, die in Zeichen oder Bytes aufgelöst werden. Diese Funktion wird in Microsoft RPC nicht unterstützt. Das [<strong>String</strong>]-Attribut kann nicht als Ganzes auf die Struktur angewendet werden. Sie kann jedoch auf jedes einzelne Array angewendet werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2192"></span><span id="midl2192"></span><dl> <dt><strong>MIDL2192</strong></dt> </dl></td>
<td><dl> <dt><span id="switch_type_can_only_be_integral__char__Boolean_or_enum"></span><span id="switch_type_can_only_be_integral__char__boolean_or_enum"></span><span id="SWITCH_TYPE_CAN_ONLY_BE_INTEGRAL__CHAR__BOOLEAN_OR_ENUM"></span>der Switchtyp kann nur eine Ganzzahl, ein Char, ein boolescher Wert oder eine Aufzählung sein</dt> <dd> Der angegebene Typ wird nicht in einen gültigen Switchtyp aufgelöst. Verwenden Sie eine Ganzzahl, ein Zeichen, einen <a href="byte.md"><strong>Byte</strong></a>, einen <a href="boolean.md"><strong>booleschen</strong></a>Wert, einen Enumerationstyp <a href="enum.md"><strong>oder einen Typ,</strong></a> der von einem dieser Typen abgeleitet ist.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2193"></span><span id="midl2193"></span><dl> <dt><strong>MIDL2193</strong></dt> </dl></td>
<td><dl> <dt><span id="_handle__must_not_be_specified_on_a_type_deriving_from_handle_t"></span><span id="_HANDLE__MUST_NOT_BE_SPECIFIED_ON_A_TYPE_DERIVING_FROM_HANDLE_T"></span>[handle] darf nicht für einen Typ angegeben werden, der von abgeleitet wird handle_t</dt> <dd> Ein Handlertyp muss mit einem und nur einem der Handlertypen oder-Attribute definiert werden. Verwenden Sie den primitiven Typ <a href="handle-t.md"><strong>handle_t</strong></a> oder das Attribut [<a href="handle.md"><strong>handle</strong></a>], aber nicht beides. Der benutzerdefinierte Handlertyp muss übertragbar sein, aber der <strong>handle_t</strong> Typ wird nicht im Netzwerk übertragen.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2194"></span><span id="midl2194"></span><dl> <dt><strong>MIDL2194</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_deriving_from_handle_t_must_not_be_an__out__parameter"></span><span id="PARAMETER_DERIVING_FROM_HANDLE_T_MUST_NOT_BE_AN__OUT__PARAMETER"></span>der Parameter, der von handle_t abgeleitet wird, darf kein [out]-Parameter sein.</dt> <dd> Ein Handle des primitiven Typs <a href="handle-t.md"><strong>handle_t</strong></a> ist nur für die Seite der Anwendung sinnvoll, in der es definiert ist. Der Typ <strong>handle_t</strong> wird nicht im Netzwerk übertragen.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2195"></span><span id="midl2195"></span><dl> <dt><strong>MIDL2195</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_expression_derives_from__unique__or__ptr__pointer_dereference"></span><span id="ATTRIBUTE_EXPRESSION_DERIVES_FROM__UNIQUE__OR__PTR__POINTER_DEREFERENCE"></span>der Attribut Ausdruck wird von [Unique] oder [PTR] Zeiger Dereferenzierung abgeleitet.</dt> <dd> Obwohl die Attribute "[<a href="unique.md"><strong>Unique</strong></a>]" und " <a href="ptr.md"><strong>Full</strong></a> " Zeiger auf <strong>null</strong> -Werte zulassen, darf der Ausdruck, der das Attribut "size" oder "length" definiert, nie einen <strong>null</strong> -Wert aufweisen. Wenn Zeiger verwendet werden, schränkt die mittlere l Ausdrücke auf [<a href="ref.md"><strong>ref</strong></a>]-Zeiger ein.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2196"></span><span id="midl2196"></span><dl> <dt><strong>MIDL2196</strong></dt> </dl></td>
<td><dl> <dt><span id="_cpp_quote__requires__ms_ext"></span><span id="_CPP_QUOTE__REQUIRES__MS_EXT"></span>&quot;cpp_quote &quot; erfordert/ms_ext</dt> <dd> Das <a href="cpp-quote.md"><strong>cpp_quote</strong></a> -Attribut ist eine Microsoft-Erweiterung für DCE IDL. Verwenden Sie nicht den Mittelwert-Compilerschalter <a href="-osf.md"><strong>/OSF</strong></a>, der überschreibt <a href="-ms-ext.md"><strong>/ms_ext</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2197"></span><span id="midl2197"></span><dl> <dt><strong>MIDL2197</strong></dt> </dl></td>
<td><dl> <dt><span id="quoted_uuid_requires__ms_ext"></span><span id="QUOTED_UUID_REQUIRES__MS_EXT"></span>uuid in Anführungszeichen erfordert/ms_ext</dt> <dd> Die Möglichkeit, einen UUID-Wert in Anführungszeichen anzugeben, ist eine Microsoft-Erweiterung für DCE IDL. Verwenden Sie nicht den Mittelwert-Compilerschalter <a href="-osf.md"><strong>/OSF</strong></a>, der überschreibt <a href="-ms-ext.md"><strong>/ms_ext</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2198"></span><span id="midl2198"></span><dl> <dt><strong>MIDL2198</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_cannot_derive_from_a_nonencapsulated_union"></span><span id="RETURN_TYPE_CANNOT_DERIVE_FROM_A_NONENCAPSULATED_UNION"></span>Rückgabetyp kann nicht aus einer nicht gekapselten Union abgeleitet</dt> <dd> Die nicht gekapselte Union kann nicht als Funktions Rückgabetyp verwendet werden. Geben Sie den Union-Typ als [<a href="out-idl.md"><strong>out</strong></a>]-oder [<strong>in, out</strong>]-Parameter an, um den Union-Typ zurückzugeben.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2199"></span><span id="midl2199"></span><dl> <dt><strong>MIDL2199</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_cannot_derive_from_a_conformant_structure"></span><span id="RETURN_TYPE_CANNOT_DERIVE_FROM_A_CONFORMANT_STRUCTURE"></span>der Rückgabetyp kann nicht von einer konformen Struktur abgeleitet werden</dt> <dd> Die Größe des Rückgabe Typs muss eine Konstante sein. Sie können nicht als Rückgabetyp eine Struktur angeben, die ein konformes Array enthält, auch wenn die Struktur auch den Größen Bezeichner enthält. Um die konforme Struktur zurückzugeben, geben Sie die Struktur als Parameter [<a href="out-idl.md"><strong>out</strong></a>] oder [<strong>in, out</strong>] an.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2200"></span><span id="midl2200"></span><dl> <dt><strong>MIDL2200</strong></dt> </dl></td>
<td><dl> <dt><span id="_transmit_as__must_not_be_applied_to_a_type_deriving_from_a_generic_handle"></span><span id="_TRANSMIT_AS__MUST_NOT_BE_APPLIED_TO_A_TYPE_DERIVING_FROM_A_GENERIC_HANDLE"></span>[Transmit_as] darf nicht auf einen Typ angewendet werden, der von einem generischen handle abgeleitet ist.</dt> <dd> In dieser Version können die Attribute [<a href="handle.md"><strong>handle</strong></a>] und [<a href="transmit-as.md"><strong>Transmit_as</strong></a>] nicht für denselben Typ kombiniert werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2201"></span><span id="midl2201"></span><dl> <dt><strong>MIDL2201</strong></dt> </dl></td>
<td><dl> <dt><span id="_handle__must_not_be_applied_to_a_type_that_has__transmit_as__applied_to_it"></span><span id="_HANDLE__MUST_NOT_BE_APPLIED_TO_A_TYPE_THAT_HAS__TRANSMIT_AS__APPLIED_TO_IT"></span>[handle] darf nicht auf einen Typ angewendet werden, auf den [Transmit_as] angewendet wurde.</dt> <dd> In dieser Version können die Attribute [<a href="handle.md"><strong>handle</strong></a>] und [<a href="transmit-as.md"><strong>Transmit_as</strong></a>] nicht für denselben Typ kombiniert werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2202"></span><span id="midl2202"></span><dl> <dt><strong>MIDL2202</strong></dt> </dl></td>
<td><dl> <dt><span id="type_specified_for_the_const_declaration_is_invalid"></span><span id="TYPE_SPECIFIED_FOR_THE_CONST_DECLARATION_IS_INVALID"></span>der für die Konstantendeklaration angegebene Typ ist ungültig.</dt> <dd> Konstante Deklarationen sind auf ganzzahlige, Zeichen-, breit Zeichen-, Zeichen folgen-und boolesche Typen beschränkt.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2203"></span><span id="midl2203"></span><dl> <dt><strong>MIDL2203</strong></dt> </dl></td>
<td><dl> <dt><span id="operand_to_the_sizeof_operator_is_not_supported"></span><span id="OPERAND_TO_THE_SIZEOF_OPERATOR_IS_NOT_SUPPORTED"></span>der Operand zum sizeof-Operator wird nicht unterstützt.</dt> <dd> Der mittlerer l-Compiler unterstützt nur den <strong>sizeof</strong> -Vorgang für einfache Typen. Der angegebene Operand wird nicht zu einem Integer-Typ ausgewertet.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2204"></span><span id="midl2204"></span><dl> <dt><strong>MIDL2204</strong></dt> </dl></td>
<td><dl> <dt><span id="this_name_already_used_as_a_const_identifier_name"></span><span id="THIS_NAME_ALREADY_USED_AS_A_CONST_IDENTIFIER_NAME"></span>Dieser Name wird bereits als Name des Konstanten Bezeichners verwendet.</dt> <dd> Der Bezeichner wurde bereits verwendet, um eine Konstante in einer <a href="const.md"><strong>Konstanten Deklaration</strong></a> zu identifizieren. Ändern Sie den Namen eines bezeichnerbezeichner, sodass die Bezeichner eindeutig sind.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2205"></span><span id="midl2205"></span><dl> <dt><strong>MIDL2205</strong></dt> </dl></td>
<td><dl> <dt><span id="inconsistent_redefinition_of_type_error_status_t"></span><span id="INCONSISTENT_REDEFINITION_OF_TYPE_ERROR_STATUS_T"></span>inkonsistente Neudefinition des Typs error_status_t</dt> <dd> Der Typ <a href="error-status-t.md"><strong>error_status_t</strong></a> muss in den Typ <strong>Ganzzahl ohne Vorzeichen long</strong>aufgelöst werden. Andere Typdefinitionen können nicht verwendet werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2206"></span><span id="midl2206"></span><dl> <dt><strong>MIDL2206</strong></dt> </dl></td>
<td><dl> <dt><span id="_case__value_out_of_range_of_switch_type"></span><span id="_CASE__VALUE_OUT_OF_RANGE_OF_SWITCH_TYPE"></span>[Case] Wert außerhalb des Bereichs des Switch-Typs</dt> <dd> Der Wert, der dem Switch-Anweisungs Fall zugeordnet ist, liegt außerhalb des gültigen Bereichs für den angegebenen Switchtyp. Dieser Fehler tritt beispielsweise auf, wenn ein Long Integer-Wert in der Case-Anweisung für einen kurzen ganzzahligen Typ verwendet wird.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2207"></span><span id="midl2207"></span><dl> <dt><strong>MIDL2207</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_deriving_from_wchar_t_needs__ms_ext"></span><span id="PARAMETER_DERIVING_FROM_WCHAR_T_NEEDS__MS_EXT"></span>Parameter, der von wchar_t Anforderungen/ms_ext abgeleitet wird</dt> <dd> Der breit Zeichentyp <a href="wchar-t.md"><strong>wchar_t</strong></a> ist eine Microsoft-Erweiterung für DCE IDL. Verwenden Sie nicht den Mittelwert-Compilerschalter <a href="-osf.md"><strong>/OSF</strong></a>, der überschreibt <a href="-ms-ext.md"><strong>/ms_ext</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2208"></span><span id="midl2208"></span><dl> <dt><strong>MIDL2208</strong></dt> </dl></td>
<td><dl> <dt><span id="this_interface_has_only_callbacks"></span><span id="THIS_INTERFACE_HAS_ONLY_CALLBACKS"></span>Diese Schnittstelle hat nur Rückrufe.</dt> <dd> Rückrufe sind nur im Kontext eines Remote Prozedur Aufrufes gültig. Die Schnittstelle muss mindestens einen Funktionsprototyp für einen Remote Prozedur Aufrufs einschließen, der das Attribut [<a href="callback.md"><strong>Callback</strong></a>] nicht enthält.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2209"></span><span id="midl2209"></span><dl> <dt><strong>MIDL2209</strong></dt> </dl></td>
<td><dl> <dt><span id="redundantly_specified_attribute__ignored"></span><span id="REDUNDANTLY_SPECIFIED_ATTRIBUTE__IGNORED"></span>redundantes Attribut angegeben; erten</dt> <dd> Das angegebene Attribut wurde mehrmals angewendet. Mehrere Instanzen desselben Attributs werden ignoriert.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2210"></span><span id="midl2210"></span><dl> <dt><strong>MIDL2210</strong></dt> </dl></td>
<td><dl> <dt><span id="context_handle_type_used_for_an_implicit_handle"></span><span id="CONTEXT_HANDLE_TYPE_USED_FOR_AN_IMPLICIT_HANDLE"></span>der für einen impliziten handle verwendete Kontext behandlertyp.</dt> <dd> Ein Typ, der mit dem [<a href="context-handle.md"><strong>context_handle</strong></a>]-Attribut definiert wurde, wurde als handle-Typ in einem [ <a href="implicit-handle.md"><strong>implicit_handle</strong></a>]-Attribut angegeben. Die Attribute können nicht auf diese Weise kombiniert werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2211"></span><span id="midl2211"></span><dl> <dt><strong>MIDL2211</strong></dt> </dl></td>
<td><dl> <dt><span id="conflicting_options_specified_for__allocate_"></span><span id="CONFLICTING_OPTIONS_SPECIFIED_FOR__ALLOCATE_"></span>für [zuordnen] werden widersprüchliche Optionen angegeben.</dt> <dd> Die für das ACF-Attribut [<a href="allocate.md"><strong>zuordnen</strong></a>] angegebenen Optionen stellen widersprüchliche Direktiven dar. Geben Sie z. b. entweder die Option all_nodes oder die Option single_node an, aber nicht beides.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2212"></span><span id="midl2212"></span><dl> <dt><strong>MIDL2212</strong></dt> </dl></td>
<td><dl> <dt><span id="error_while_writing_to_file"></span><span id="ERROR_WHILE_WRITING_TO_FILE"></span>Fehler beim Schreiben in die Datei.</dt> <dd> Fehler beim Schreiben in die Datei. Diese Bedingung kann durch Fehler im Zusammenhang mit Speicherplatz, Datei Handles, Datei Zugriffsbeschränkungen und Hardwarefehlern verursacht werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2213"></span><span id="midl2213"></span><dl> <dt><strong>MIDL2213</strong></dt> </dl></td>
<td><dl> <dt><span id="no_switch_type_found_at_definition_of_union__using_the__switch_is__type"></span><span id="NO_SWITCH_TYPE_FOUND_AT_DEFINITION_OF_UNION__USING_THE__SWITCH_IS__TYPE"></span>in der Definition von Union wurde kein Switchtyp mit dem [Switch_is]-Typ gefunden.</dt> <dd> Die Union-Definition enthält kein explizites [<a href="switch-type.md"><strong>Switch_type</strong></a>]-Attribut. Der Typ der Variablen, die vom [<a href="switch-is.md"><strong>Switch_is</strong></a>]-Attribut angegeben wird, wird als Switchtyp verwendet.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2214"></span><span id="midl2214"></span><dl> <dt><strong>MIDL2214</strong></dt> </dl></td>
<td><dl> <dt><span id="semantic_check_incomplete_due_to_previous_errors"></span><span id="SEMANTIC_CHECK_INCOMPLETE_DUE_TO_PREVIOUS_ERRORS"></span>die semantische Prüfung ist aufgrund vorheriger Fehler unvollständig.</dt> <dd> Der-Mittell-Compiler nimmt zwei Durchgänge an den Eingabedateien an, um vorwärts Deklarationen aufzulösen. Aufgrund von Fehlern, die beim ersten Durchlauf aufgetreten sind, wurde die Überprüfung auf den zweiten Durchlauf nicht durchgeführt. Nicht gemeldete Fehler im Zusammenhang mit vorwärts Deklarationen können in der Datei weiterhin vorhanden sein.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2215"></span><span id="midl2215"></span><dl> <dt><strong>MIDL2215</strong></dt> </dl></td>
<td><dl> <dt><span id="handle_parameter_or_return_type_is_not_supported_on_a__callback__procedure"></span><span id="HANDLE_PARAMETER_OR_RETURN_TYPE_IS_NOT_SUPPORTED_ON_A__CALLBACK__PROCEDURE"></span>handle-Parameter oder Rückgabetyp werden für eine [Callback]-Prozedur nicht unterstützt.</dt> <dd> Eine [<a href="callback.md"><strong>Callback</strong></a>]-Prozedur tritt im Kontext eines Aufrufs von einem Client zum Server auf und verwendet das gleiche Bindungs handle wie der ursprüngliche-Befehl. Explizite Bindungs handle-Parameter oder Rückgabe Typen sind in Rückruf Funktionen nicht zulässig.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2216"></span><span id="midl2216"></span><dl> <dt><strong>MIDL2216</strong></dt> </dl></td>
<td><dl> <dt><span id="_ptr__does_not_support_aliasing_in_this_version"></span><span id="_PTR__DOES_NOT_SUPPORT_ALIASING_IN_THIS_VERSION"></span>[PTR] unterstützt in dieser Version kein Aliasing.</dt> <dd> Ein Alias tritt auf, wenn über mehr als einen Zeiger-oder Variablennamen auf Daten zugegriffen werden kann. Entfernen Sie den Alias. Weitere Informationen finden Sie unter <a href="/windows/desktop/Rpc/unique-pointers">Unique-Zeiger</a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2217"></span><span id="midl2217"></span><dl> <dt><strong>MIDL2217</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_already_defined_as_a_context_handle"></span><span id="PARAMETER_ALREADY_DEFINED_AS_A_CONTEXT_HANDLE"></span>der Parameter ist bereits als Kontext Handle definiert.</dt> <dd> Der-Parameter wurde zuvor als Kontext Handle definiert.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2218"></span><span id="midl2218"></span><dl> <dt><strong>MIDL2218</strong></dt> </dl></td>
<td><dl> <dt><span id="_context_handle__must_not_derive_from_handle_t"></span><span id="_CONTEXT_HANDLE__MUST_NOT_DERIVE_FROM_HANDLE_T"></span>[context_handle] darf nicht von abgeleitet werden handle_t</dt> <dd> Die drei handle-Merkmale: der Typ <a href="handle-t.md"><strong>handle_t</strong></a>, das Attribut [<a href="handle.md"><strong>handle</strong></a>] und das Attribut [<a href="context-handle.md"><strong>context_handle</strong></a>] schließen sich gegenseitig aus. Es kann jeweils nur ein Merkmal auf einen Typ oder Parameter angewendet werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2219"></span><span id="midl2219"></span><dl> <dt><strong>MIDL2219</strong></dt> </dl></td>
<td><dl> <dt><span id="array_size_exceeds_65536_bytes"></span><span id="ARRAY_SIZE_EXCEEDS_65536_BYTES"></span>die Array Größe überschreitet 65536 Bytes.</dt> <dd> Auf einigen Plattformen von Microsoft beträgt die maximale Datengröße von 64 KB. Entwerfen Sie Ihre Anwendung so neu, dass alle übertragenen Daten in die maximal zulässige Größe passen.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2220"></span><span id="midl2220"></span><dl> <dt><strong>MIDL2220</strong></dt> </dl></td>
<td><dl> <dt><span id="structure_size_exceeds_65536_bytes"></span><span id="STRUCTURE_SIZE_EXCEEDS_65536_BYTES"></span>die Struktur Größe überschreitet 65536 Bytes.</dt> <dd> Auf einigen Plattformen von Microsoft beträgt die maximale Datengröße von 64 KB. Entwerfen Sie Ihre Anwendung so neu, dass alle übertragenen Daten in die maximal zulässige Größe passen.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2221"></span><span id="midl2221"></span><dl> <dt><strong>MIDL2221</strong></dt> </dl></td>
<td><dl> <dt><span id="field_of_a_nonencapsulated_union_cannot_be_another_nonencapsulated_union"></span><span id="FIELD_OF_A_NONENCAPSULATED_UNION_CANNOT_BE_ANOTHER_NONENCAPSULATED_UNION"></span>das Feld einer nicht gekapselten Union darf keine andere nicht gekapselte Union sein</dt> <dd> Unions, die als Teil eines Remote Prozedur Aufrufes übertragen werden, benötigen ein zugeordnetes Datenelement, das diskriminant, das den Union Arm auswählt. Unions, die in andere Unions eingebettet sind, bieten keine unter Diskriminante. Daher können Sie in dieser Form nicht übertragen werden. Erstellen Sie eine Struktur, die aus der Union und deren diskriminant besteht.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2222"></span><span id="midl2222"></span><dl> <dt><strong>MIDL2222</strong></dt> </dl></td>
<td><dl> <dt><span id="pointer_attribute_s__applied_on_an_embedded_array__ignored"></span><span id="POINTER_ATTRIBUTE_S__APPLIED_ON_AN_EMBEDDED_ARRAY__IGNORED"></span>Zeiger Attribute, die auf ein eingebettetes Array angewendet werden; erten</dt> <dd> Ein Zeiger Attribut kann nur auf ein Array angewendet werden, wenn es sich bei dem Array um einen Parameter der obersten Ebene handelt. Andere Zeiger Attribute, die auf in andere Datenstrukturen eingebettete Arrays angewendet werden, werden ignoriert.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2223"></span><span id="midl2223"></span><dl> <dt><strong>MIDL2223</strong></dt> </dl></td>
<td><dl> <dt><span id="_allocate__is_illegal_on_either_the_transmitted_or_presented_type_for__transmit_as____represent_as____wire_marshal___or__user_marshal_"></span><span id="_ALLOCATE__IS_ILLEGAL_ON_EITHER_THE_TRANSMITTED_OR_PRESENTED_TYPE_FOR__TRANSMIT_AS____REPRESENT_AS____WIRE_MARSHAL___OR__USER_MARSHAL_"></span>[zuordnen] ist entweder für den übertragenen oder dargestellten Typ für [Transmit_as], [represent_as], [Wire_marshal] oder [user_marshal] unzulässig.</dt> <dd> Die Attribute [<a href="transmit-as.md"><strong>Transmit_as</strong></a>] und [<a href="allocate.md"><strong>zuordnen</strong></a>] können nicht gleichzeitig auf denselben Typ angewendet werden. Das [<strong>Transmit_as</strong>]-Attribut unterscheidet zwischen dargestellten und übertragenen Typen, während<strong>das [Attribut</strong>]-Attribut annimmt, dass der dargestellte Typ mit dem übertragenen Typ identisch ist.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2224"></span><span id="midl2224"></span><dl> <dt><strong>MIDL2224</strong></dt> </dl></td>
<td>[Switch_type] muss in diesem Import Modus angegeben werden.<br/></td>
</tr>
<tr class="even">
<td><span id="MIDL2225"></span><span id="midl2225"></span><dl> <dt><strong>MIDL2225</strong></dt> </dl></td>
<td><dl> <dt><span id="_implicit_handle__type_undefined__assuming_generic_handle"></span><span id="_IMPLICIT_HANDLE__TYPE_UNDEFINED__ASSUMING_GENERIC_HANDLE"></span>[implicit_handle] Typ nicht definiert. angenommen, generisches Handle</dt> <dd> Der in der ACF angegebene Handlertyp ist nicht in der IDL-Datei definiert. Der mittlerer l-Compiler geht davon aus, dass der Handle-Typ in den primitiven Handle-Typ <a href="handle-t.md"><strong>handle_t</strong></a>aufgelöst wird. Fügen Sie der Typdefinition das Attribut [<a href="handle.md"><strong>handle</strong></a>] hinzu, wenn sich das Handle wie ein benutzerdefiniertes oder generisches Handle Verhalten soll.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2226"></span><span id="midl2226"></span><dl> <dt><strong>MIDL2226</strong></dt> </dl></td>
<td><dl> <dt><span id="array_element_must_not_derive_from_error_status_t"></span><span id="ARRAY_ELEMENT_MUST_NOT_DERIVE_FROM_ERROR_STATUS_T"></span>Das Array Element darf nicht von error_status_t abgeleitet werden.</dt> <dd> In dieser Version von Microsoft RPC kann der Typ <a href="error-status-t.md"><strong>error_status_t</strong></a> nur als Parameter oder Rückgabetyp angezeigt werden. Er kann nicht in Arrays angezeigt werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2227"></span><span id="midl2227"></span><dl> <dt><strong>MIDL2227</strong></dt> </dl></td>
<td><dl> <dt><span id="_allocate__illegal_on_a_type_deriving_from_a_primitive_generic_context_handle"></span><span id="_ALLOCATE__ILLEGAL_ON_A_TYPE_DERIVING_FROM_A_PRIMITIVE_GENERIC_CONTEXT_HANDLE"></span>[zuordnen] unzulässig für einen Typ, der von einem primitiven/generischen/Kontext Handle abgeleitet ist.</dt> <dd> Das ACF-Attribut [<a href="allocate.md"><strong>zuordnen</strong></a>] kann nicht auf Typen angewendet werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2228"></span><span id="midl2228"></span><dl> <dt><strong>MIDL2228</strong></dt> </dl></td>
<td><dl> <dt><span id="transmitted_or_presented_type_must_not_derive_from_error_status_t"></span><span id="TRANSMITTED_OR_PRESENTED_TYPE_MUST_NOT_DERIVE_FROM_ERROR_STATUS_T"></span>der übertragene oder präsentierte Typ darf nicht von error_status_t abgeleitet werden.</dt> <dd> In dieser Version von Microsoft RPC kann der Typ <a href="error-status-t.md"><strong>error_status_t</strong></a> nicht mit dem [<a href="transmit-as.md"><strong>Transmit_as</strong></a>]-Attribut verwendet werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2229"></span><span id="midl2229"></span><dl> <dt><strong>MIDL2229</strong></dt> </dl></td>
<td><dl> <dt><span id="discriminant_of_a_union_must_not_derive_from_a_field_with__ignore__applied_to_it"></span><span id="DISCRIMINANT_OF_A_UNION_MUST_NOT_DERIVE_FROM_A_FIELD_WITH__IGNORE__APPLIED_TO_IT"></span>die Diskriminante einer Union darf nicht von einem Feld abgeleitet werden, auf das [Ignore] angewendet wurde.</dt> <dd> Eine Union, die in einem Remote Prozedur Aufruf verwendet wird, muss einem anderen Datenelement zugeordnet werden, das als diskriminant bezeichnet wird, das den Union Arm auswählt. Der diskriminant muss übertragen werden. Das [<a href="ignore.md"><strong>Ignore</strong></a>]-Attribut kann nicht auf den Union-Diskriminanten angewendet werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2230"></span><span id="midl2230"></span><dl> <dt><strong>MIDL2230</strong></dt> </dl></td>
<td><dl> <dt><span id="_nocode__ignored_for_server_side_since___server_none__not_specified"></span><span id="_NOCODE__IGNORED_FOR_SERVER_SIDE_SINCE___SERVER_NONE__NOT_SPECIFIED"></span>[NoCode] wird für serverseitig ignoriert, da &quot; /Server None &quot; nicht angegeben ist.</dt> <dd> Einige DCE-IDL-Compiler generieren einen Fehler, wenn das [<a href="nocode.md"><strong>NoCode</strong></a>]-Attribut auf eine Prozedur in einer Schnittstelle angewendet wird, für die Server-Stub-Dateien generiert werden. Da der Server alle Vorgänge unterstützen muss, muss [<strong>NoCode</strong>] nicht auf eine Prozedur in diesem Modus angewendet werden, oder Sie müssen den Mittelwert des Compilerschalters <a href="-server.md"><strong>/Server</strong></a> None verwenden, um explizit anzugeben, dass keine Server Routinen generiert werden sollen.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2231"></span><span id="midl2231"></span><dl> <dt><strong>MIDL2231</strong></dt> </dl></td>
<td><dl> <dt><span id="no_remote_procedures_specified_in_non-_local__interface__no_client_server_stubs_will_be_generated"></span><span id="NO_REMOTE_PROCEDURES_SPECIFIED_IN_NON-_LOCAL__INTERFACE__NO_CLIENT_SERVER_STUBS_WILL_BE_GENERATED"></span>in einer nicht-[local]-Schnittstelle sind keine Remote Prozeduren angegeben. Es werden keine Client-/serverstubstubweise generiert</dt> <dd> Die bereitgestellte Schnittstelle verfügt über keine Remote Prozeduren, sodass nur Header Dateien generiert werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2232"></span><span id="midl2232"></span><dl> <dt><strong>MIDL2232</strong></dt> </dl></td>
<td><dl> <dt><span id="too_many_default_cases_specified_for_encapsulated_union"></span><span id="TOO_MANY_DEFAULT_CASES_SPECIFIED_FOR_ENCAPSULATED_UNION"></span>zu viele Standardfälle für die gekapselte Union angegeben</dt> <dd> Eine gekapselte Union kann nur einen Standardwert aufweisen: Arm.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2233"></span><span id="midl2233"></span><dl> <dt><strong>MIDL2233</strong></dt> </dl></td>
<td><dl> <dt><span id="too_many_default_interfaces_specified_for_coclass"></span><span id="TOO_MANY_DEFAULT_INTERFACES_SPECIFIED_FOR_COCLASS"></span>zu viele Standardschnittstellen für die Co-Klasse angegeben.</dt> <dd> Eine <a href="coclass.md"><strong>Co-Klasse</strong></a> kann höchstens zwei [<a href="default.md"><strong>default</strong></a>]-Member haben, eine zur Darstellung der ausgehenden (Quell-) Schnittstelle oder dispinterface, und eine, die die eingehende (Senke) Schnittstelle oder dispinterface darstellt.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2234"></span><span id="midl2234"></span><dl> <dt><strong>MIDL2234</strong></dt> </dl></td>
<td><dl> <dt><span id="items_with__defaultvtable__must_also_have__source_"></span><span id="ITEMS_WITH__DEFAULTVTABLE__MUST_ALSO_HAVE__SOURCE_"></span>Elemente mit [defaultvtable] müssen auch [Quelle] aufweisen.</dt> <dd> Die <a href="defaultvtable.md"><strong>defaultvtable</strong></a> -Schnittstelle erstellt eine zweite Quell Schnittstelle für ein Objekt, mit dem senken Ereignisse über die V-Tabelle empfangen können.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2235"></span><span id="midl2235"></span><dl> <dt><strong>MIDL2235</strong></dt> </dl></td>
<td><dl> <dt><span id="union_specification_with_no_fields_is_illegal"></span><span id="UNION_SPECIFICATION_WITH_NO_FIELDS_IS_ILLEGAL"></span>die Union-Spezifikation ohne Felder ist unzulässig.</dt> <dd> Unions müssen mindestens ein Feld haben.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2236"></span><span id="midl2236"></span><dl> <dt><strong>MIDL2236</strong></dt> </dl></td>
<td><dl> <dt><span id="value_out_of_range"></span><span id="VALUE_OUT_OF_RANGE"></span>Wert außerhalb des zulässigen Bereichs</dt> <dd> Der angegebene Case-Wert liegt außerhalb des Bereichs des Switchtyps.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2237"></span><span id="midl2237"></span><dl> <dt><strong>MIDL2237</strong></dt> </dl></td>
<td><dl> <dt><span id="_context_handle__must_be_applied_on_a_pointer_type"></span><span id="_CONTEXT_HANDLE__MUST_BE_APPLIED_ON_A_POINTER_TYPE"></span>[context_handle] muss auf einen Zeigertyp angewendet werden.</dt> <dd> Kontext Handles müssen immer Zeiger Typen sein. DCE gibt an, dass alle Kontext Handles als <strong>void *</strong>typisiert werden müssen.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2238"></span><span id="midl2238"></span><dl> <dt><strong>MIDL2238</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_must_not_derive_from_handle_t"></span><span id="RETURN_TYPE_MUST_NOT_DERIVE_FROM_HANDLE_T"></span>der Rückgabetyp darf nicht von handle_t abgeleitet werden.</dt> <dd><a href="handle-t.md"><strong>handle_t</strong></a> kann nicht zurückgegeben werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2239"></span><span id="midl2239"></span><dl> <dt><strong>MIDL2239</strong></dt> </dl></td>
<td><dl> <dt><span id="_handle__must_not_be_applied_to_a_type_deriving_from_a_context_handle"></span><span id="_HANDLE__MUST_NOT_BE_APPLIED_TO_A_TYPE_DERIVING_FROM_A_CONTEXT_HANDLE"></span>[handle] darf nicht auf einen Typ angewendet werden, der von einem Kontext Handle abgeleitet ist.</dt> <dd> Ein Typ kann nicht gleichzeitig ein Kontext Handle und ein generisches Handle sein.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2240"></span><span id="midl2240"></span><dl> <dt><strong>MIDL2240</strong></dt> </dl></td>
<td><dl> <dt><span id="field_deriving_from_an__int__must_have_size_specifier__small____short___or__long__with_the__int_"></span><span id="FIELD_DERIVING_FROM_AN__INT__MUST_HAVE_SIZE_SPECIFIER__SMALL____SHORT___OR__LONG__WITH_THE__INT_"></span>das von einem int abgeleitete Feld &quot; &quot; muss den Größen Bezeichner " &quot; Small", "Short" oder " &quot; &quot; &quot; &quot; Long &quot; &quot; " aufweisen.&quot;</dt> <dd> Der Typ " <a href="int.md"><strong>int</strong></a> " ist auf 16-Bit-Systemen nicht zulässig, da sich die Größe von " <strong>int</strong> " auf mehreren Computern unterscheiden kann.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2241"></span><span id="midl2241"></span><dl> <dt><strong>MIDL2241</strong></dt> </dl></td>
<td><dl> <dt><span id="field_must_not_derive_from_a_void_or_void__"></span><span id="FIELD_MUST_NOT_DERIVE_FROM_A_VOID_OR_VOID__"></span>Feld darf nicht von void oder void abgeleitet werden *</dt> <dd> <strong>void</strong> und <strong>void *</strong> können nicht als Parametertypen für Remote Prozeduren verwendet werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2242"></span><span id="midl2242"></span><dl> <dt><strong>MIDL2242</strong></dt> </dl></td>
<td><dl> <dt><span id="field_must_not_derive_from_a_structure_containing_bit-fields"></span><span id="FIELD_MUST_NOT_DERIVE_FROM_A_STRUCTURE_CONTAINING_BIT-FIELDS"></span>das Feld darf nicht von einer Struktur abgeleitet werden, die Bitfelder enthält.</dt> <dd> Strukturen, die Bitfelder enthalten, können nicht als Parameter oder Rückgabe Typen für Remote Prozeduren verwendet werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2243"></span><span id="midl2243"></span><dl> <dt><strong>MIDL2243</strong></dt> </dl></td>
<td><dl> <dt><span id="field_must_not_derive_from_a_non-rpcable_union"></span><span id="FIELD_MUST_NOT_DERIVE_FROM_A_NON-RPCABLE_UNION"></span>das Feld darf nicht von einer nicht-rpcable-Union abgeleitet werden.</dt> <dd> Eine Union muss als nicht gekapselte Union oder gekapselte Union angegeben werden, damit Sie übertragen werden können. Bei normalen C-Unions fehlt der diskriminant, der zum Übertragen der Union über das Netzwerk erforderlich ist.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2244"></span><span id="midl2244"></span><dl> <dt><strong>MIDL2244</strong></dt> </dl></td>
<td><dl> <dt><span id="field_must_not_derive_from_a_pointer_to_a_function"></span><span id="FIELD_MUST_NOT_DERIVE_FROM_A_POINTER_TO_A_FUNCTION"></span>das Feld darf nicht von einem Zeiger auf eine Funktion abgeleitet werden.</dt> <dd> Zeiger auf Funktionen können nicht an Remote Prozeduren übertragen werden. Zeiger auf Funktionen zeigen auf Funktionscode, und es kann kein Funktionscode über das Netzwerk mithilfe von RPC übertragen werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2245"></span><span id="midl2245"></span><dl> <dt><strong>MIDL2245</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_use__fault_status__on_both_a_parameter_and_a_return_type"></span><span id="CANNOT_USE__FAULT_STATUS__ON_BOTH_A_PARAMETER_AND_A_RETURN_TYPE"></span>[fault_status] kann nicht für einen Parameter und einen Rückgabetyp verwendet werden.</dt> <dd> Das Attribut [<a href="fault-status.md"><strong>fault_status</strong></a>] kann nur einmal pro Prozedur verwendet werden. Das [<a href="comm-status.md"><strong>comm_status</strong></a>]-Attribut kann unabhängig verwendet werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2246"></span><span id="midl2246"></span><dl> <dt><strong>MIDL2246</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_too_complicated_for__Oi_modes__using__Os"></span><span id="return_type_too_complicated_for__oi_modes__using__os"></span><span id="RETURN_TYPE_TOO_COMPLICATED_FOR__OI_MODES__USING__OS"></span>der Rückgabetyp ist zu kompliziert für/Oi-Modi mit/OS</dt> <dd> Große Rückgabe Typen, die als Wert übermittelt werden, können nur durch <a href="-os.md"><strong>/OS</strong></a> -Optimierungs-stubwerte behandelt werden. Die stusb für diese Routine werden mithilfe der <strong>/OS</strong> -Optimierung generiert.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2247"></span><span id="midl2247"></span><dl> <dt><strong>MIDL2247</strong></dt> </dl></td>
<td><dl> <dt><span id="generic_handle_type_too_large_for__Oi_modes__using__Os"></span><span id="generic_handle_type_too_large_for__oi_modes__using__os"></span><span id="GENERIC_HANDLE_TYPE_TOO_LARGE_FOR__OI_MODES__USING__OS"></span>generischer Handlertyp zu groß für/Oi-Modi mit/OS</dt> <dd> Große generische handle-Typen, die als Wert übermittelt werden, können nur durch <a href="-os.md"><strong>/OS</strong></a> -Optimierungs stubwerte behandelt werden. Die stusb für diese Routine werden mithilfe der <strong>/OS</strong> -Optimierung generiert.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2248"></span><span id="midl2248"></span><dl> <dt><strong>MIDL2248</strong></dt> </dl></td>
<td><dl> <dt><span id="_allocate_all_nodes___on_an__in_out__parameter_may_orphan_the_original_memory"></span><span id="_ALLOCATE_ALL_NODES___ON_AN__IN_OUT__PARAMETER_MAY_ORPHAN_THE_ORIGINAL_MEMORY"></span>[zuordnen (all_nodes)] für einen [in, out]-Parameter kann den ursprünglichen Arbeitsspeicher verwaist.</dt> <dd> Die Verwendung von [Zuordnungs<a href="allocate.md"><strong>(all_nodes</strong></a>)] für einen [<a href="in.md"><strong>in</strong></a>, <a href="out-idl.md"><strong>out</strong></a>]-Parameter muss zusammenhängenden Speicher für die [<strong>out</strong>]-Richtung zuordnen und somit den [<strong>in</strong>]-Parameter verwaisen. Diese Verwendung ist nicht empfehlenswert.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2249"></span><span id="midl2249"></span><dl> <dt><strong>MIDL2249</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_have_a__ref__pointer_as_a_union_arm"></span><span id="CANNOT_HAVE_A__REF__POINTER_AS_A_UNION_ARM"></span>ein [REF]-Zeiger kann nicht als Union Arm vorhanden sein.</dt> <dd> Verweis Zeiger müssen immer auf gültigen Speicher zeigen, aber eine [<a href="in.md"><strong>in</strong></a>, <a href="out-idl.md"><strong>out</strong></a>]-Union mit einem Verweis Zeiger kann einen Verweis Zeiger zurückgeben, wenn die [<strong>in</strong>]-Richtung einen anderen Typ verwendet.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2250"></span><span id="midl2250"></span><dl> <dt><strong>MIDL2250</strong></dt> </dl></td>
<td><dl> <dt><span id="return_of_context_handles_not_supported_for__Oi_modes__using__Os"></span><span id="return_of_context_handles_not_supported_for__oi_modes__using__os"></span><span id="RETURN_OF_CONTEXT_HANDLES_NOT_SUPPORTED_FOR__OI_MODES__USING__OS"></span>Rückgabe von Kontext Handles, die für/Oi-Modi nicht unterstützt werden, mithilfe von/OS</dt> <dd> Die-Mittell unterstützt keine Kontext Handles in den voll interpretierten Optimierungs Modi. Wechseln zur Optimierung im gemischten Modus.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2251"></span><span id="midl2251"></span><dl> <dt><strong>MIDL2251</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_the_extra__comm_status__or__fault_status__parameter_not_supported_for__Oi_modes__using__Os"></span><span id="use_of_the_extra__comm_status__or__fault_status__parameter_not_supported_for__oi_modes__using__os"></span><span id="USE_OF_THE_EXTRA__COMM_STATUS__OR__FAULT_STATUS__PARAMETER_NOT_SUPPORTED_FOR__OI_MODES__USING__OS"></span>die Verwendung des Parameters "extra [comm_status]" oder "[fault_status]" wird für/Oi-Modi mit/OS nicht unterstützt.</dt> <dd> Die Attribute [<a href="comm-status.md"><strong>comm_status</strong></a>] und [<a href="fault-status.md"><strong>fault_status</strong></a>] können nur von <a href="-os.md"><strong>/OS</strong></a> Optimization-stubarbeiten behandelt werden. Die stusb für diese Routine werden mithilfe der <strong>/OS</strong> -Optimierung generiert.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2252"></span><span id="midl2252"></span><dl> <dt><strong>MIDL2252</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_an_unknown_type_for__represent_as__or__user_marshal__not_supported_for__Oi_modes__using__Os"></span><span id="use_of_an_unknown_type_for__represent_as__or__user_marshal__not_supported_for__oi_modes__using__os"></span><span id="USE_OF_AN_UNKNOWN_TYPE_FOR__REPRESENT_AS__OR__USER_MARSHAL__NOT_SUPPORTED_FOR__OI_MODES__USING__OS"></span>die Verwendung eines unbekannten Typs für [represent_as] oder [user_marshal] wird für/Oi-Modi mithilfe von/OS nicht unterstützt.</dt> <dd> Die Verwendung des [<a href="represent-as.md"><strong>represent_as</strong></a>]-Attributs mit einem lokalen Typ, der nicht in der IDL-Datei definiert ist, oder einer importierten IDL-Datei kann nur durch <a href="-os.md"><strong>/OS</strong></a> -Optimierungs-stubvorgänge behandelt werden. Die stusb für diese Routine werden mithilfe der <strong>/OS</strong> -Optimierung generiert.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2253"></span><span id="midl2253"></span><dl> <dt><strong>MIDL2253</strong></dt> </dl></td>
<td><dl> <dt><span id="array_types_with__transmit_as__or__represent_as__not_supported_on_return_type_for__Oi_modes___using__Os"></span><span id="array_types_with__transmit_as__or__represent_as__not_supported_on_return_type_for__oi_modes___using__os"></span><span id="ARRAY_TYPES_WITH__TRANSMIT_AS__OR__REPRESENT_AS__NOT_SUPPORTED_ON_RETURN_TYPE_FOR__OI_MODES___USING__OS"></span>Array Typen mit [Transmit_as] oder [represent_as] werden für den Rückgabetyp für/Oi-Modi mithilfe von/OS nicht unterstützt.</dt> <dd> Das Zurückgeben eines Arrays mit "[<a href="transmit-as.md"><strong>Transmit_as</strong></a>]" oder "[<a href="represent-as.md"><strong>represent_as</strong></a>]" ist nur durch <a href="-os.md"><strong>/OS</strong></a> Optimization stubweise möglich. Die stusb für diese Routine werden mithilfe der <strong>/OS</strong> -Optimierung generiert.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2254"></span><span id="midl2254"></span><dl> <dt><strong>MIDL2254</strong></dt> </dl></td>
<td><dl> <dt><span id="array_types_with__transmit_as__or__represent_as__not_supported_pass-by-value_for__Oi_modes__using__Os"></span><span id="array_types_with__transmit_as__or__represent_as__not_supported_pass-by-value_for__oi_modes__using__os"></span><span id="ARRAY_TYPES_WITH__TRANSMIT_AS__OR__REPRESENT_AS__NOT_SUPPORTED_PASS-BY-VALUE_FOR__OI_MODES__USING__OS"></span>Array Typen mit [Transmit_as] oder [represent_as] werden für/Oi-Modi mit/OS nicht unterstützt.</dt> <dd> Diese Aktion wird für die vollständig interpretierte Optimierung nicht unterstützt. Wechseln zur Optimierung im gemischten Modus.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2255"></span><span id="midl2255"></span><dl> <dt><strong>MIDL2255</strong></dt> </dl></td>
<td><dl> <dt><span id="_callback__requires__ms_ext"></span><span id="_CALLBACK__REQUIRES__MS_EXT"></span>[Rückruf] erfordert/ms_ext</dt> <dd> Das [<a href="callback.md"><strong>Callback</strong></a>]-Attribut ist eine Microsoft-Erweiterung und erfordert, dass der Schalter <a href="-ms-ext.md"><strong>/ms_ext</strong></a> aktiviert ist. Kompilieren Sie nicht mit <a href="-osf.md"><strong>/OSF</strong></a>, was überschreibt <strong>/ms_ext</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2256"></span><span id="midl2256"></span><dl> <dt><strong>MIDL2256</strong></dt> </dl></td>
<td><dl> <dt><span id="circular_interface_dependency"></span><span id="CIRCULAR_INTERFACE_DEPENDENCY"></span>zirkuläre Schnittstellen Abhängigkeit</dt> <dd> Diese Schnittstelle verwendet sich selbst (direkt oder indirekt) als Basisschnittstelle.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2257"></span><span id="midl2257"></span><dl> <dt><strong>MIDL2257</strong></dt> </dl></td>
<td><dl> <dt><span id="only_IUnknown_may_be_used_as_the_root_interface"></span><span id="only_iunknown_may_be_used_as_the_root_interface"></span><span id="ONLY_IUNKNOWN_MAY_BE_USED_AS_THE_ROOT_INTERFACE"></span>nur IUnknown kann als Stamm Schnittstelle verwendet werden.</dt> <dd> Derzeit müssen alle Schnittstellen <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a> als Stamm Schnittstelle haben.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2258"></span><span id="midl2258"></span><dl> <dt><strong>MIDL2258</strong></dt> </dl></td>
<td><dl> <dt><span id="_IID_IS__may_only_be_applied_to_pointers_to_interfaces"></span><span id="_iid_is__may_only_be_applied_to_pointers_to_interfaces"></span><span id="_IID_IS__MAY_ONLY_BE_APPLIED_TO_POINTERS_TO_INTERFACES"></span>[IID_IS] darf nur auf Zeiger auf Schnittstellen angewendet werden.</dt> <dd> Das [<a href="iid-is.md"><strong>iid_is</strong></a>]-Attribut kann nur auf Schnittstellen Zeiger angewendet werden, obwohl Sie als Zeiger auf <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a> * angegeben werden können.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2259"></span><span id="midl2259"></span><dl> <dt><strong>MIDL2259</strong></dt> </dl></td>
<td><dl> <dt><span id="interfaces_may_only_be_used_in_pointer-to-interface_constructs"></span><span id="INTERFACES_MAY_ONLY_BE_USED_IN_POINTER-TO-INTERFACE_CONSTRUCTS"></span>Schnittstellen können nur in Zeiger-zu-Schnittstellen-Konstrukten verwendet werden.</dt> <dd> Schnittstellennamen können nur als Basis Schnittstellen oder Schnittstellen Zeiger verwendet werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2260"></span><span id="midl2260"></span><dl> <dt><strong>MIDL2260</strong></dt> </dl></td>
<td><dl> <dt><span id="interface_pointers_must_have_a_UUID_IID"></span><span id="interface_pointers_must_have_a_uuid_iid"></span><span id="INTERFACE_POINTERS_MUST_HAVE_A_UUID_IID"></span>Schnittstellen Zeiger müssen eine UUID/IID aufweisen.</dt> <dd> Der Basistyp des [<a href="iid-is.md"><strong>iid_is</strong></a>]-Ausdrucks muss ein UUID/GUID/IID-Typ sein.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2261"></span><span id="midl2261"></span><dl> <dt><strong>MIDL2261</strong></dt> </dl></td>
<td><dl> <dt><span id="definitions_and_declarations_outside_of_interface_body_requires__ms_ext"></span><span id="DEFINITIONS_AND_DECLARATIONS_OUTSIDE_OF_INTERFACE_BODY_REQUIRES__MS_EXT"></span>Definitionen und Deklarationen außerhalb des Schnittstellen Texts erfordern/ms_ext</dt> <dd> Das Einfügen von Deklarationen und Definitionen außerhalb eines beliebigen Schnittstellen Texts ist eine Microsoft-Erweiterung und erfordert die Verwendung des Schalters <a href="-ms-ext.md"><strong>/ms_ext</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2262"></span><span id="midl2262"></span><dl> <dt><strong>MIDL2262</strong></dt> </dl></td>
<td><dl> <dt><span id="multiple_interfaces_in_one_file_requires__ms_ext"></span><span id="MULTIPLE_INTERFACES_IN_ONE_FILE_REQUIRES__MS_EXT"></span>mehrere Schnittstellen in einer Datei erfordern/ms_ext</dt> <dd> Die Verwendung mehrerer Schnittstellen in einer einzelnen IDL-Datei ist eine Microsoft-Erweiterung und nicht verfügbar, wenn Sie im <a href="-osf.md"><strong>/OSF</strong></a> -Modus kompilieren.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2263"></span><span id="midl2263"></span><dl> <dt><strong>MIDL2263</strong></dt> </dl></td>
<td><dl> <dt><span id="only_one_of__implicit_handle____auto_handle___or__explicit_handle__allowed"></span><span id="ONLY_ONE_OF__IMPLICIT_HANDLE____AUTO_HANDLE___OR__EXPLICIT_HANDLE__ALLOWED"></span>nur eine von [implicit_handle], [auto_handle] oder [explicit_handle] ist zulässig.</dt> <dd> Jede Schnittstelle kann nur eines dieser drei Attribute aufweisen.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2264"></span><span id="midl2264"></span><dl> <dt><strong>MIDL2264</strong></dt> </dl></td>
<td><dl> <dt><span id="_implicit_handle__references_a_type_which_is_not_a_handle"></span><span id="_IMPLICIT_HANDLE__REFERENCES_A_TYPE_WHICH_IS_NOT_A_HANDLE"></span>[implicit_handle] verweist auf einen Typ, der kein Handle ist.</dt> <dd> Implizite Handles müssen einen der Handlertypen aufweisen.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2265"></span><span id="midl2265"></span><dl> <dt><strong>MIDL2265</strong></dt> </dl></td>
<td><dl> <dt><span id="_object__procs_may_only_be_used_with___env_win32_"></span><span id="_OBJECT__PROCS_MAY_ONLY_BE_USED_WITH___ENV_WIN32_"></span>[Object] Prozeduren suchen dürfen nur mit/env Win32 verwendet werden. &quot;&quot;</dt> <dd> Schnittstellen mit dem Attribut [<a href="object.md"><strong>Object</strong></a>] können nicht mit 16-Bit-Umgebungen verwendet werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2266"></span><span id="midl2266"></span><dl> <dt><strong>MIDL2266</strong></dt> </dl></td>
<td><dl> <dt><span id="_callback__with_-env_dos_win16_not_supported_for__Oi__using__Os"></span><span id="_callback__with_-env_dos_win16_not_supported_for__oi__using__os"></span><span id="_CALLBACK__WITH_-ENV_DOS_WIN16_NOT_SUPPORTED_FOR__OI__USING__OS"></span>[Callback] mit-"DOS/Win16" wird für/Oi mit/OS nicht unterstützt.</dt> <dd> Rückrufe in 16-Bit-Umgebungen können nur durch <a href="-os.md"><strong>/OS</strong></a> -Optimierungs-stubwerte verarbeitet werden. Die stusb für diese Routine werden mithilfe der <strong>/OS</strong> -Optimierung generiert.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2267"></span><span id="midl2267"></span><dl> <dt><strong>MIDL2267</strong></dt> </dl></td>
<td><dl> <dt><span id="float_double_not_supported_as_top-level_parameter_for__Oi_mode__using__Os"></span><span id="float_double_not_supported_as_top-level_parameter_for__oi_mode__using__os"></span><span id="FLOAT_DOUBLE_NOT_SUPPORTED_AS_TOP-LEVEL_PARAMETER_FOR__OI_MODE__USING__OS"></span>float/double wird als Parameter der obersten Ebene für den/Oi-Modus unter Verwendung von/OS nicht unterstützt.</dt> <dd> Die Typen "float" und "Double" können nur von den <a href="-os.md"><strong>/OS</strong></a> -Optimierungs stubparametern als Parameter behandelt werden. Die stusb für diese Routine werden mithilfe der <strong>/OS</strong> -Optimierung generiert. Die Typen "float" und "Double" innerhalb von Strukturen, Arrays oder Unions können weiterhin mit<strong>/OS</strong>behandelt werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2268"></span><span id="midl2268"></span><dl> <dt><strong>MIDL2268</strong></dt> </dl></td>
<td><dl> <dt><span id="pointers_to_context_handles_may_not_be_used_as_return_values"></span><span id="POINTERS_TO_CONTEXT_HANDLES_MAY_NOT_BE_USED_AS_RETURN_VALUES"></span>Zeiger auf Kontext Handles dürfen nicht als Rückgabewerte verwendet werden.</dt> <dd> Kontext Handles müssen als direkte Rückgabewerte, nicht als indirekte Rückgabewerte verwendet werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2269"></span><span id="midl2269"></span><dl> <dt><strong>MIDL2269</strong></dt> </dl></td>
<td><dl> <dt><span id="procedures_in_an_object_interface_must_return_an_HRESULT"></span><span id="procedures_in_an_object_interface_must_return_an_hresult"></span><span id="PROCEDURES_IN_AN_OBJECT_INTERFACE_MUST_RETURN_AN_HRESULT"></span>Prozeduren in einer Objektschnittstelle müssen ein HRESULT zurückgeben.</dt> <dd> Alle Prozeduren in einer Objektschnittstelle, die nicht über das-[<a href="local.md"><strong>local</strong></a>]-Attribut verfügen, müssen einen <strong>HRESULT</strong>- / <strong>SCODE</strong>zurückgeben.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2270"></span><span id="midl2270"></span><dl> <dt><strong>MIDL2270</strong></dt> </dl></td>
<td><dl> <dt><span id="duplicate_UUID"></span><span id="duplicate_uuid"></span><span id="DUPLICATE_UUID"></span>doppelte UUID.</dt> <dd> Wie UUIDs müssen eindeutig sein.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2271"></span><span id="midl2271"></span><dl> <dt><strong>MIDL2271</strong></dt> </dl></td>
<td><dl> <dt><span id="_object__interfaces_must_derive_from_another__object__interface_such_as_IUnknown"></span><span id="_object__interfaces_must_derive_from_another__object__interface_such_as_iunknown"></span><span id="_OBJECT__INTERFACES_MUST_DERIVE_FROM_ANOTHER__OBJECT__INTERFACE_SUCH_AS_IUNKNOWN"></span>[Object]-Schnittstellen müssen von einer anderen [Object]-Schnittstelle abgeleitet werden, z.b. IUnknown</dt> <dd> Die Schnittstellen Vererbung ist nur zulässig, wenn Sie Objekt Schnittstellen verwenden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2272"></span><span id="midl2272"></span><dl> <dt><strong>MIDL2272</strong></dt> </dl></td>
<td><dl> <dt><span id="_async__interface_must_derive_from_another__async__interface"></span><span id="_ASYNC__INTERFACE_MUST_DERIVE_FROM_ANOTHER__ASYNC__INTERFACE"></span>(Async) die Schnittstelle muss von einer anderen (Async) Schnittstelle abgeleitet werden.</dt> <dd> Objekt Schnittstellen (synchron und asynchron) müssen von <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a> oder einer anderen Basis-OLE-Schnittstelle abgeleitet werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2273"></span><span id="midl2273"></span><dl> <dt><strong>MIDL2273</strong></dt> </dl></td>
<td><dl> <dt><span id="_IID_IS__expression_must_be_a_pointer_to_IID_structure"></span><span id="_iid_is__expression_must_be_a_pointer_to_iid_structure"></span><span id="_IID_IS__EXPRESSION_MUST_BE_A_POINTER_TO_IID_STRUCTURE"></span>[IID_IS] Ausdruck muss ein Zeiger auf die IID-Struktur sein.</dt> <dd> Der Basistyp des [<a href="iid-is.md"><strong>iid_is</strong></a>]-Ausdrucks muss ein UUID/GUID/IID-Typ sein.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2274"></span><span id="midl2274"></span><dl> <dt><strong>MIDL2274</strong></dt> </dl></td>
<td><dl> <dt><span id="_call_as__type_must_be_a__local__procedure"></span><span id="_CALL_AS__TYPE_MUST_BE_A__LOCAL__PROCEDURE"></span>[Call_as] der Typ muss eine [local]-Prozedur sein.</dt> <dd> Auf das Ziel eines [<a href="call-as.md"><strong>Call_as</strong></a>]-Typs muss, sofern definiert, [ <a href="local.md"><strong>local</strong></a>] angewendet werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2275"></span><span id="midl2275"></span><dl> <dt><strong>MIDL2275</strong></dt> </dl></td>
<td><dl> <dt><span id="undefined__call_as__must_not_be_used_in_an_object_interface"></span><span id="UNDEFINED__CALL_AS__MUST_NOT_BE_USED_IN_AN_OBJECT_INTERFACE"></span>nicht definiertes [Call_as] darf nicht in einer Objektschnittstelle verwendet werden.</dt> <dd> Sie müssen das Ziel eines [<a href="call-as.md"><strong>Call_as</strong></a>]-Typs definieren. Stellen Sie sicher, dass Sie <strong>Call_as</strong> Routinen für die aufrufenden und aufgerufenen Anwendungen bereitgestellt haben.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2276"></span><span id="midl2276"></span><dl> <dt><strong>MIDL2276</strong></dt> </dl></td>
<td><dl> <dt><span id="_auto_handle__may_not_be_used_with__encode__or__decode_"></span><span id="_AUTO_HANDLE__MAY_NOT_BE_USED_WITH__ENCODE__OR__DECODE_"></span>[auto_handle] darf nicht mit [codieren] oder [decodieren] verwendet werden.</dt> <dd> Die Attribute [ <a href="encode.md"><strong>Codieren</strong></a>] und [ <a href="decode.md"><strong>decodieren</strong></a>] können nur mit expliziten Handles oder impliziten Handles verwendet werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2277"></span><span id="midl2277"></span><dl> <dt><strong>MIDL2277</strong></dt> </dl></td>
<td><dl> <dt><span id="normal_procedures_are_not_allowed_in_an_interface_with__encode__or__decode_"></span><span id="NORMAL_PROCEDURES_ARE_NOT_ALLOWED_IN_AN_INTERFACE_WITH__ENCODE__OR__DECODE_"></span>Normale Prozeduren sind in einer Schnittstelle mit [Encode] oder [Decode] nicht zulässig.</dt> <dd> Schnittstellen, die [<a href="encode.md"><strong>Codieren</strong></a>]-oder [<a href="decode.md"><strong>decodieren</strong></a>]-Prozeduren enthalten, können nicht auch über Remote<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2278"></span><span id="midl2278"></span><dl> <dt><strong>MIDL2278</strong></dt> </dl></td>
<td><dl> <dt><span id="top-level_conformance_or_variance_not_allowed_with__encode__or__decode_"></span><span id="TOP-LEVEL_CONFORMANCE_OR_VARIANCE_NOT_ALLOWED_WITH__ENCODE__OR__DECODE_"></span>Konformität oder Varianz der höchsten Ebene mit [codieren] oder [decodieren] nicht zulässig</dt> <dd> Typen, die die Übereinstimmung auf oberster Ebene oder Varianz aufweisen, können die Typserialisierung nicht verwenden, da es keine Möglichkeit gibt, die Größenanpassung/Verlängerung bereitzustellen. Strukturen, die Sie enthalten, sind jedoch für die Verwendung der Typserialisierung zulässig.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2279"></span><span id="midl2279"></span><dl> <dt><strong>MIDL2279</strong></dt> </dl></td>
<td><dl> <dt><span id="_out__parameters_may_not_have__const_"></span><span id="_OUT__PARAMETERS_MAY_NOT_HAVE__CONST_"></span>[out] Parameter dürfen nicht &quot; konstant sein.&quot;</dt> <dd> Da ein [<a href="out-idl.md"><strong>out</strong></a>]-Parameter geändert wird, darf er nicht als SA-Konstante deklariert werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2280"></span><span id="midl2280"></span><dl> <dt><strong>MIDL2280</strong></dt> </dl></td>
<td><dl> <dt><span id="return_values_may_not_have__const_"></span><span id="RETURN_VALUES_MAY_NOT_HAVE__CONST_"></span>Rückgabewerte dürfen nicht &quot; konstant sein.&quot;</dt> <dd> Da bei der Rückgabe der Funktion ein Funktionswert festgelegt wird, darf dieser Wert nicht als Konstante deklariert werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2281"></span><span id="midl2281"></span><dl> <dt><strong>MIDL2281</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid_use_of__retval__attribute"></span><span id="INVALID_USE_OF__RETVAL__ATTRIBUTE"></span>Ungültige Verwendung des &quot; retval- &quot; Attributs.</dt> <dd> Stellen Sie sicher, dass Sie das [<a href="optional.md"><strong>optional</strong></a>]-Attribut nicht verwendet haben und dass der [<a href="retval.md"><strong>retval</strong></a>]-Parameter der letzte Parameter in der Liste ist.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2282"></span><span id="midl2282"></span><dl> <dt><strong>MIDL2282</strong></dt> </dl></td>
<td><dl> <dt><span id="multiple_calling_conventions_illegal"></span><span id="MULTIPLE_CALLING_CONVENTIONS_ILLEGAL"></span>mehrere Aufruf Konventionen sind unzulässig.</dt> <dd> Nur eine Aufruf Konvention kann auf eine einzelne Prozedur angewendet werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2283"></span><span id="midl2283"></span><dl> <dt><strong>MIDL2283</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_illegal_on__object__procedure"></span><span id="ATTRIBUTE_ILLEGAL_ON__OBJECT__PROCEDURE"></span>ungültiges Attribut für [Object]-Prozedur</dt> <dd> Das obige Attribut gilt nur für Prozeduren in Schnittstellen, die nicht über das [<a href="object.md"><strong>Object</strong></a>]-Attribut verfügen.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2284"></span><span id="midl2284"></span><dl> <dt><strong>MIDL2284</strong></dt> </dl></td>
<td><dl> <dt><span id="_out__interface_pointers_must_use_double_indirection"></span><span id="_OUT__INTERFACE_POINTERS_MUST_USE_DOUBLE_INDIRECTION"></span>[out] Schnittstellen Zeiger müssen doppelte Dereferenzierung verwenden.</dt> <dd> Da der geänderte Wert der Zeiger auf die-Schnittstelle ist, muss eine andere Dereferenzierungsebene oberhalb des Zeigers vorhanden sein, damit diese zurückgegeben werden kann.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2285"></span><span id="midl2285"></span><dl> <dt><strong>MIDL2285</strong></dt> </dl></td>
<td><dl> <dt><span id="procedure_used_twice_as_the_caller_in__call_as_"></span><span id="PROCEDURE_USED_TWICE_AS_THE_CALLER_IN__CALL_AS_"></span>Prozedur, die zweimal als Aufrufer in [Call_as] verwendet wird</dt> <dd> Eine bestimmte [<a href="local.md"><strong>local</strong></a>]-Prozedur kann nur einmal als Ziel eines [<a href="call-as.md"><strong>Call_as</strong></a>] verwendet werden, um Namenskonflikte zu vermeiden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2286"></span><span id="midl2286"></span><dl> <dt><strong>MIDL2286</strong></dt> </dl></td>
<td><dl> <dt><span id="_call_as__target_must_have__local__in_an_object_interface"></span><span id="_CALL_AS__TARGET_MUST_HAVE__LOCAL__IN_AN_OBJECT_INTERFACE"></span>[Call_as] Ziel muss [local] in einer Objektschnittstelle enthalten.</dt> <dd> Das Ziel eines [<a href="call-as.md"><strong>Call_as</strong></a>] muss eine definierte [<a href="local.md"><strong>local</strong></a>]-Prozedur in der aktuellen-Schnittstelle sein.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2287"></span><span id="midl2287"></span><dl> <dt><strong>MIDL2287</strong></dt> </dl></td>
<td><dl> <dt><span id="_code__and__nocode__may_not_be_used_together"></span><span id="_CODE__AND__NOCODE__MAY_NOT_BE_USED_TOGETHER"></span>[Code] und [NoCode] können nicht gleichzeitig verwendet werden.</dt> <dd> Diese beiden Attribute sind widersprüchlich und können nicht gleichzeitig verwendet werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2288"></span><span id="midl2288"></span><dl> <dt><strong>MIDL2288</strong></dt> </dl></td>
<td><dl> <dt><span id="procedures_with__maybe__or__message__attributes_may_not_have__out__params__or_return_values_must_be_of_type_HRESULT_or_error_status_t"></span><span id="procedures_with__maybe__or__message__attributes_may_not_have__out__params__or_return_values_must_be_of_type_hresult_or_error_status_t"></span><span id="PROCEDURES_WITH__MAYBE__OR__MESSAGE__ATTRIBUTES_MAY_NOT_HAVE__OUT__PARAMS__OR_RETURN_VALUES_MUST_BE_OF_TYPE_HRESULT_OR_ERROR_STATUS_T"></span>Prozeduren mit den Attributen [Maybe] oder [Message] haben möglicherweise keine [out]-Parameter, oder Rückgabewerte müssen vom Typ HRESULT oder error_status_t</dt> <dd> Da [<a href="maybe.md"><strong>vielleicht</strong></a>] Prozeduren nie zurückgeben, gibt es keine Möglichkeit, Rückgabewerte zu erhalten.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2289"></span><span id="midl2289"></span><dl> <dt><strong>MIDL2289</strong></dt> </dl></td>
<td><dl> <dt><span id="pointer_to_function_must_be_used"></span><span id="POINTER_TO_FUNCTION_MUST_BE_USED"></span>Ein Zeiger auf eine Funktion muss verwendet werden.</dt> <dd> Obwohl Funktionstyp Definitionen im <a href="-c-ext.md"><strong>/c_ext</strong></a> Modus zulässig sind, können Sie nur als Zeiger auf Funktionen verwendet werden. Sie können niemals als Parameter oder Rückgabewert einer Remote Prozedur übertragen werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2290"></span><span id="midl2290"></span><dl> <dt><strong>MIDL2290</strong></dt> </dl></td>
<td><dl> <dt><span id="functions_may_not_be_passed_in_an_RPC_operation"></span><span id="functions_may_not_be_passed_in_an_rpc_operation"></span><span id="FUNCTIONS_MAY_NOT_BE_PASSED_IN_AN_RPC_OPERATION"></span>Funktionen können nicht in einem RPC-Vorgang übermittelt werden.</dt> <dd> Funktionen und Funktionszeiger können nicht als Parameter oder Rückgabewerte von Remote Prozeduren weitergegeben werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2291"></span><span id="midl2291"></span><dl> <dt><strong>MIDL2291</strong></dt> </dl></td>
<td><dl> <dt><span id="hyper_double_not_supported_as_return_value_for__Oi_modes__using__Os"></span><span id="hyper_double_not_supported_as_return_value_for__oi_modes__using__os"></span><span id="HYPER_DOUBLE_NOT_SUPPORTED_AS_RETURN_VALUE_FOR__OI_MODES__USING__OS"></span>Hyper/Double wird als Rückgabewert für/Oi-Modi mit/OS nicht unterstützt.</dt> <dd> Hyperund Double-Rückgabewerte können nur durch <a href="-os.md"><strong>/OS</strong></a> -Optimierungs stubwerte behandelt werden. Die stusb für diese Routine werden mithilfe der <strong>/OS</strong> -Optimierung generiert.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2292"></span><span id="midl2292"></span><dl> <dt><strong>MIDL2292</strong></dt> </dl></td>
<td><dl> <dt><span id="_pragma_pack_pop__without_matching__pragma_pack_push_"></span><span id="_PRAGMA_PACK_POP__WITHOUT_MATCHING__PRAGMA_PACK_PUSH_"></span>#Pragma Pack (Pop) ohne übereinstimmendes #Pragma Pack (Push)</dt> <dd> #Pragma Pack (Push) und #Pragma Pack (Pop) müssen in übereinstimmenden Paaren angezeigt werden. Es wurden mindestens eine zu viele #Pragma Pack-(Push) s angegeben.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2293"></span><span id="midl2293"></span><dl> <dt><strong>MIDL2293</strong></dt> </dl></td>
<td><dl> <dt><span id="stringable_structure_fields_must_be_byte_char_wchar_t"></span><span id="STRINGABLE_STRUCTURE_FIELDS_MUST_BE_BYTE_CHAR_WCHAR_T"></span>stringable-Struktur Felder müssen Byte/char/wchar_t sein</dt> <dd> Der Typ [<a href="string.md"><strong>String</strong></a>] kann nur auf eine Struktur angewendet werden, deren Felder alle vom Typ Byte sind, oder eine Typdefinition, die Byte entspricht.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2294"></span><span id="midl2294"></span><dl> <dt><strong>MIDL2294</strong></dt> </dl></td>
<td><dl> <dt><span id="_notify__not_supported_for__Oi_modes__using__Os"></span><span id="_notify__not_supported_for__oi_modes__using__os"></span><span id="_NOTIFY__NOT_SUPPORTED_FOR__OI_MODES__USING__OS"></span>[notify] wird für/Oi-Modi mit/OS nicht unterstützt.</dt> <dd> Das [<a href="notify.md"><strong>Notify</strong></a>]-Attribut kann nur von <a href="-os.md"><strong>/OS</strong></a> Optimization-stubweisen verarbeitet werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2295"></span><span id="midl2295"></span><dl> <dt><strong>MIDL2295</strong></dt> </dl></td>
<td><dl> <dt><span id="_handle_parameter_or_return_type_is_not_supported_on_a_procedure_in_an__object__interface"></span><span id="_HANDLE_PARAMETER_OR_RETURN_TYPE_IS_NOT_SUPPORTED_ON_A_PROCEDURE_IN_AN__OBJECT__INTERFACE"></span> handle-Parameter oder Rückgabetyp werden für eine Prozedur in einer [Object]-Schnittstelle nicht unterstützt.</dt> <dd> Handles können nicht mit [ <a href="object.md"><strong>Object</strong></a>]-Schnittstellen verwendet werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2296"></span><span id="midl2296"></span><dl> <dt><strong>MIDL2296</strong></dt> </dl></td>
<td><dl> <dt><span id="ANSI_C_only_allows_the_leftmost_array_bound_to_be_unspecified"></span><span id="ansi_c_only_allows_the_leftmost_array_bound_to_be_unspecified"></span><span id="ANSI_C_ONLY_ALLOWS_THE_LEFTMOST_ARRAY_BOUND_TO_BE_UNSPECIFIED"></span>In ANSI C ist es nur möglich, dass das Array ganz links als nicht angegeben festgelegt ist.</dt> <dd> In einem konformen Array ermöglicht ANSI C nur, dass das ganz links-Array (signifikanteste Array) nicht angegeben wird. Wenn mehrere Dimensionen konform sind, versucht die Mittel l, eine &quot; 1 &quot; in den anderen konformen Dimensionen abzulegen. Wenn die anderen Dimensionen in einer anderen Typdefinition definiert sind, ist dies nicht möglich. Versuchen Sie, alle Array Dimensionen in der Array Deklaration zu platzieren, um dies zu vermeiden. Beachten Sie in jedem Fall die Array Indizierungs Berechnungen, die vom Compiler durchgeführt wurden. Möglicherweise müssen Sie Ihre eigenen Berechnungen mit den tatsächlichen Größen durchführen.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2297"></span><span id="midl2297"></span><dl> <dt><strong>MIDL2297</strong></dt> </dl></td>
<td><dl> <dt><span id="by-value_union_parameters_not_supported_for__Oi_modes__using__Os"></span><span id="by-value_union_parameters_not_supported_for__oi_modes__using__os"></span><span id="BY-VALUE_UNION_PARAMETERS_NOT_SUPPORTED_FOR__OI_MODES__USING__OS"></span>by-Value-Union-Parameter werden für/Oi-Modi mithilfe von/OS nicht unterstützt.</dt> <dd> Diese Aktion wird für die vollständig interpretierte Optimierung nicht unterstützt. Wechseln zur Optimierung im gemischten Modus.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2298"></span><span id="midl2298"></span><dl> <dt><strong>MIDL2298</strong></dt> </dl></td>
<td><dl> <dt><span id="_version__attribute_is_ignored_on_an__object__interface"></span><span id="_VERSION__ATTRIBUTE_IS_IGNORED_ON_AN__OBJECT__INTERFACE"></span>[Version] das Attribut wird in einer [Object]-Schnittstelle ignoriert.</dt> <dd> Das Attribut [<a href="object.md"><strong>Object</strong></a>] identifiziert eine COM-Schnittstelle. Eine Schnittstellen Attribut Liste für eine COM-Schnittstelle kann das Attribut [ <a href="version.md"><strong>Version</strong></a>] nicht enthalten.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2299"></span><span id="midl2299"></span><dl> <dt><strong>MIDL2299</strong></dt> </dl></td>
<td><dl> <dt><span id="_size_is__or__max_is__attribute_is_invalid_on_a_fixed_array"></span><span id="_SIZE_IS__OR__MAX_IS__ATTRIBUTE_IS_INVALID_ON_A_FIXED_ARRAY"></span>Das [size_is]-oder [Max_is]-Attribut ist für ein festes Array ungültig.</dt> <dd> Arrays mit fester Größe können die Attribute " <a href="size-is.md"><strong>size_is</strong></a> " oder " <a href="max-is.md"><strong>Max_is</strong></a> " nicht verwenden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2300"></span><span id="midl2300"></span><dl> <dt><strong>MIDL2300</strong></dt> </dl></td>
<td><dl> <dt><span id="_encode__or__decode__are_invalid_in_an__object__interface"></span><span id="_ENCODE__OR__DECODE__ARE_INVALID_IN_AN__OBJECT__INTERFACE"></span>[Encode] oder [Decode] sind in einer [Object]-Schnittstelle ungültig.</dt> <dd> Das Attribut [<a href="object.md"><strong>Object</strong></a>] identifiziert eine COM-Schnittstelle. Die Attribute [<a href="encode.md"><strong>Codieren</strong></a>] und [ <a href="decode.md"><strong>decodieren</strong></a>] ermöglichen die Serialisierung. Das heißt, Sie können Puffer für das Mars Hallen und das Entsperren von Daten bereitstellen und steuern. Sie können jedoch keine Serialisierung für COM-Schnittstellen durchführen.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2301"></span><span id="midl2301"></span><dl> <dt><strong>MIDL2301</strong></dt> </dl></td>
<td><dl> <dt><span id="_encode__or__decode__on_a_type_requires__ms_ext"></span><span id="_ENCODE__OR__DECODE__ON_A_TYPE_REQUIRES__MS_EXT"></span>[codieren] oder [Decode] für einen Typ erfordert/ms_ext</dt> <dd> Die Serialisierung ist nicht Teil der DCE-IDL-Spezifikation. Dabei handelt es sich um eine Microsoft-Erweiterung, die die Verwendung des Befehls Zeilenschalters <a href="-ms-ext.md"><strong>/ms_ext</strong></a> erfordert.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2302"></span><span id="midl2302"></span><dl> <dt><strong>MIDL2302</strong></dt> </dl></td>
<td><dl> <dt><span id="int_not_supported_on__env_win16_or__env_dos"></span><span id="INT_NOT_SUPPORTED_ON__ENV_WIN16_OR__ENV_DOS"></span>"int" wird auf/env Win16 oder/env DOS nicht unterstützt.</dt> <dd> Die 16-Bit-Microsoft-Plattformen unterstützen nicht die Verwendung des Typs " <a href="int.md"><strong>int</strong></a> " in einer IDL-Datei. Qualifizieren Sie den <strong>int</strong> -Typ mit <a href="small.md"><strong>Small</strong></a>, <a href="short.md"><strong>Short</strong></a>oder <a href="long.md"><strong>Long</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2303"></span><span id="midl2303"></span><dl> <dt><strong>MIDL2303</strong></dt> </dl></td>
<td><dl> <dt><span id="_bstring__may_only_be_applied_to_a_pointer_to__char__or__whchar_t_"></span><span id="_BSTRING__MAY_ONLY_BE_APPLIED_TO_A_POINTER_TO__CHAR__OR__WHCHAR_T_"></span>[bString] kann nur auf einen Zeiger auf &quot; Char &quot; oder &quot; whchar_t angewendet werden.&quot;</dt> <dd> Dieser Fehler ist veraltet. Sie wird nur aus Gründen der Abwärtskompatibilität bereitgestellt.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2304"></span><span id="midl2304"></span><dl> <dt><strong>MIDL2304</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_invalid_on_a_procedure_in_an__object__interface"></span><span id="ATTRIBUTE_INVALID_ON_A_PROCEDURE_IN_AN__OBJECT__INTERFACE"></span>ungültiges Attribut für eine Prozedur in einer [Object]-Schnittstelle.</dt> <dd> Das angegebene Attribut ist für die Prozedur in einer COM-Schnittstelle nicht zulässig.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2305"></span><span id="midl2305"></span><dl> <dt><strong>MIDL2305</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_invalid_on_an__object__interface"></span><span id="ATTRIBUTE_INVALID_ON_AN__OBJECT__INTERFACE"></span>ungültiges Attribut für eine [Object]-Schnittstelle.</dt> <dd> Das angegebene Attribut ist in einer COM-Schnittstelle nicht zulässig.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2306"></span><span id="midl2306"></span><dl> <dt><strong>MIDL2306</strong></dt> </dl></td>
<td><dl> <dt><span id="too_many_parameters_or_stack_too_big_for__Oi_modes__using__Os"></span><span id="too_many_parameters_or_stack_too_big_for__oi_modes__using__os"></span><span id="TOO_MANY_PARAMETERS_OR_STACK_TOO_BIG_FOR__OI_MODES__USING__OS"></span>zu viele Parameter oder Stapel zu groß für/Oi-Modi mit/OS</dt> <dd> Diese Warnung ist veraltet. Sie wird nur aus Gründen der Abwärtskompatibilität bereitgestellt. Es zeigt an, dass der Remote Prozedur Aufrufe bewirkt, dass der Stapel größer als 64 K wird.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2307"></span><span id="midl2307"></span><dl> <dt><strong>MIDL2307</strong></dt> </dl></td>
<td><dl> <dt><span id="no_attributes_on_ACF_file_typedef__so_no_effect"></span><span id="no_attributes_on_acf_file_typedef__so_no_effect"></span><span id="NO_ATTRIBUTES_ON_ACF_FILE_TYPEDEF__SO_NO_EFFECT"></span>keine Attribute in der ACF-Datei-typedef, keine Auswirkung</dt> <dd> Die IDL-Datei sollte alle typedef-Anweisungen enthalten, die keine Attribute aufweisen. Sie sollten nicht in ACF-Dateien auftreten. Wenn dies der Fall ist, interpretiert der mittlerer l-Compiler Sie als redundant und ignoriert Sie.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2308"></span><span id="midl2308"></span><dl> <dt><strong>MIDL2308</strong></dt> </dl></td>
<td><dl> <dt><span id="calling_conventions_other_than___stdcall_or___cdecl_not_supported_for__Oi_modes__using__Os"></span><span id="calling_conventions_other_than___stdcall_or___cdecl_not_supported_for__oi_modes__using__os"></span><span id="CALLING_CONVENTIONS_OTHER_THAN___STDCALL_OR___CDECL_NOT_SUPPORTED_FOR__OI_MODES__USING__OS"></span>andere Aufruf Konventionen als __stdcall oder __cdecl werden für/Oi-Modi mithilfe von/OS nicht unterstützt.</dt> <dd> Aufruf Konventionen, z. b. <strong>__pascal</strong> oder <strong>__fastcall</strong> , ändern das Format des Stapels. Die <a href="-oi.md"><strong>/Oi</strong></a> -Modi unterstützen nur die <strong>__stdcall</strong> -und <strong>__cdecl</strong> Aufruf Konventionen. Wenn Sie andere Aufruf Konventionen verwenden müssen, verwenden Sie den <a href="-os.md"><strong>/OS</strong></a> -Modus.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2309"></span><span id="midl2309"></span><dl> <dt><strong>MIDL2309</strong></dt> </dl></td>
<td><dl> <dt><span id="Too_many_delegation_methods_in_the_interface__require_Windows_2000_or_greater"></span><span id="too_many_delegation_methods_in_the_interface__require_windows_2000_or_greater"></span><span id="TOO_MANY_DELEGATION_METHODS_IN_THE_INTERFACE__REQUIRE_WINDOWS_2000_OR_GREATER"></span>Zu viele Delegierungs Methoden in der Schnittstelle, erfordern Windows 2000 oder höher.</dt> <dd> Eine Schnittstelle kann von einer anderen Schnittstelle erben. Wenn dies der Fall ist, gelten die Methoden der Basisschnittstelle als delegiert. Keine abgeleitete Schnittstelle kann mehr als 256 Delegierte Methoden enthalten.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2310"></span><span id="midl2310"></span><dl> <dt><strong>MIDL2310</strong></dt> </dl></td>
<td><dl> <dt><span id="auto_handles_not_supported_with__env_mac_or__env_powermac"></span><span id="AUTO_HANDLES_NOT_SUPPORTED_WITH__ENV_MAC_OR__ENV_POWERMAC"></span>Automatische Handles werden bei/env Mac oder/env PowerMac nicht unterstützt.</dt> <dd> Beim Kompilieren der IDL-Datei für einen PowerMac können keine automatischen Bindungs Handles verwendet werden. Sie müssen explizite oder implizite Handles angeben.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2311"></span><span id="midl2311"></span><dl> <dt><strong>MIDL2311</strong></dt> </dl></td>
<td><dl> <dt><span id="statements_outside_library_block_are_illegal_in_mktyplib_compatibility_mode"></span><span id="STATEMENTS_OUTSIDE_LIBRARY_BLOCK_ARE_ILLEGAL_IN_MKTYPLIB_COMPATIBILITY_MODE"></span>Anweisungen außerhalb des Bibliotheks Blocks sind im MkTypLib-Kompatibilitätsmodus unzulässig.</dt> <dd> Beim Kompilieren der IDL-Datei müssen Sie möglicherweise den <a href="-mktyplib203.md"><strong>/mktyplib203</strong></a> -Befehlszeilen Schalter angeben.<br/>
<blockquote>
[!Note]<br />
Das Mktyplib.exe Tool ist veraltet. Verwenden Sie stattdessen den Mittel l-Compiler.
</blockquote>
<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2312"></span><span id="midl2312"></span><dl> <dt><strong>MIDL2312</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_syntax_unless_using_mktyplib_compatibility_mode"></span><span id="ILLEGAL_SYNTAX_UNLESS_USING_MKTYPLIB_COMPATIBILITY_MODE"></span>Ungültige Syntax, wenn der MkTypLib-Kompatibilitätsmodus nicht</dt> <dd> Beim Kompilieren der IDL-Datei müssen Sie möglicherweise den <a href="-mktyplib203.md"><strong>/mktyplib203</strong></a> -Befehlszeilen Schalter angeben.<br/>
<blockquote>
[!Note]<br />
Das Mktyplib.exe Tool ist veraltet. Verwenden Sie stattdessen den Mittel l-Compiler.
</blockquote>
<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2313"></span><span id="midl2313"></span><dl> <dt><strong>MIDL2313</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_definition__must_use_typedef_in_mktyplib_compatibility_mode"></span><span id="ILLEGAL_DEFINITION__MUST_USE_TYPEDEF_IN_MKTYPLIB_COMPATIBILITY_MODE"></span>Ungültige Definition, muss typedef im MkTypLib-Kompatibilitätsmodus verwenden.</dt> <dd> Beim Kompilieren der IDL-Datei müssen Sie möglicherweise den <a href="-mktyplib203.md"><strong>/mktyplib203</strong></a> -Befehlszeilen Schalter angeben.<br/>
<blockquote>
[!Note]<br />
Das Mktyplib.exe Tool ist veraltet. Verwenden Sie stattdessen den Mittel l-Compiler.
</blockquote>
<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2314"></span><span id="midl2314"></span><dl> <dt><strong>MIDL2314</strong></dt> </dl></td>
<td><dl> <dt><span id="explicit_pointer_attribute__ptr___ref__ignored_for_interface_pointers"></span><span id="EXPLICIT_POINTER_ATTRIBUTE__PTR___REF__IGNORED_FOR_INTERFACE_POINTERS"></span>explizites Zeiger Attribut [PTR] [REF] wird für Schnittstellen Zeiger ignoriert.</dt> <dd> Zeiger auf Schnittstellen können keine IDL-Attribute aufweisen.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2315"></span><span id="midl2315"></span><dl> <dt><strong>MIDL2315</strong></dt> </dl></td>
<td><a href="-oi.md"><strong>/Oi</strong></a> -Modi, die für PowerMac nicht implementiert wurden, wechseln zu <a href="-os.md"> <strong>/OS</strong></a><br/></td>
</tr>
<tr class="odd">
<td><span id="MIDL2316"></span><span id="midl2316"></span><dl> <dt><strong>MIDL2316</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_expression_type_used_in_attribute"></span><span id="ILLEGAL_EXPRESSION_TYPE_USED_IN_ATTRIBUTE"></span>Ungültiger Ausdruckstyp in Attribut verwendet.</dt> <dd> Der Standardwert für den Zeiger sollte eine Konstante sein.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2317"></span><span id="midl2317"></span><dl> <dt><strong>MIDL2317</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_type_used_in_pipe"></span><span id="ILLEGAL_TYPE_USED_IN_PIPE"></span>Unzulässiger Typ in Pipe verwendet</dt> <dd> Pipes sind auf einfache IDL-Datentypen beschränkt. Sie können z. b. keine Pipe von Arrays angeben.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2318"></span><span id="midl2318"></span><dl> <dt><strong>MIDL2318</strong></dt> </dl></td>
<td><dl> <dt><span id="procedure_uses_pipes__using__Oicf"></span><span id="procedure_uses_pipes__using__oicf"></span><span id="PROCEDURE_USES_PIPES__USING__OICF"></span>Prozedur verwendet Pipes mithilfe von/Oicf</dt> <dd> Der Modus, den Sie ausgewählt haben, unterstützt keine Pipes. Der mittlerer l-Compiler hat die Verwendung eines oder mehrerer Pipes in der Schnittstelle erkannt. Daher wird die IDL-Datei im <a href="-oi.md"><strong>/Oicf</strong></a> -Modus kompiliert.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2319"></span><span id="midl2319"></span><dl> <dt><strong>MIDL2319</strong></dt> </dl></td>
<td><dl> <dt><span id="procedure_has_an_attribute_that_requires_use_of__Oif__switching_modes"></span><span id="procedure_has_an_attribute_that_requires_use_of__oif__switching_modes"></span><span id="PROCEDURE_HAS_AN_ATTRIBUTE_THAT_REQUIRES_USE_OF__OIF__SWITCHING_MODES"></span>die Prozedur verfügt über ein Attribut, das die Verwendung von/OIF-und Wechsel Modi erfordert.</dt> <dd> Sie müssen [<a href="async.md"><strong>Async</strong></a>]-Prozeduren im <a href="-oi.md"><strong>/OIF</strong></a> -Modus kompilieren.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2320"></span><span id="midl2320"></span><dl> <dt><strong>MIDL2320</strong></dt> </dl></td>
<td><dl> <dt><span id="conflicting_optimization_requirements__cannot_optimize"></span><span id="CONFLICTING_OPTIMIZATION_REQUIREMENTS__CANNOT_OPTIMIZE"></span>in Konflikt stehende Optimierungs Anforderungen, kann nicht optimiert werden</dt> <dd> Dieser Fehler gibt häufig an, dass Sie sowohl <a href="-os.md"><strong>/OS</strong></a> als auch <a href="-oi.md"><strong>/Oi</strong></a> (oder eine Variante von <strong>/Oi</strong>)-compilermodi angegeben haben. Dies kann auch bedeuten, dass die Funktionen, die Sie in ihren IDL-und ACL-Dateien angegeben haben, beide Modi verwenden müssen. Sie müssen einen oder den anderen Modus auswählen, um zu optimieren.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2321"></span><span id="midl2321"></span><dl> <dt><strong>MIDL2321</strong></dt> </dl></td>
<td><dl> <dt><span id="pipes_cannot_be_array_elements__or_members_of_structures_or_unions"></span><span id="PIPES_CANNOT_BE_ARRAY_ELEMENTS__OR_MEMBERS_OF_STRUCTURES_OR_UNIONS"></span>Pipes können keine Array Elemente oder Mitglieder von Strukturen oder Unions sein.</dt> <dd> Pipedatentypen können nur Parameter der obersten Ebene sein.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2322"></span><span id="midl2322"></span><dl> <dt><strong>MIDL2322</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid_pipe_usage"></span><span id="INVALID_PIPE_USAGE"></span>Ungültige Pipe-Verwendung</dt> <dd> Pipes können nicht mit den Attributen [<a href="transmit-as.md"><strong>Transmit_as</strong></a>], [<a href="represent-as.md"><strong>represent_as</strong></a>] oder [<a href="user-marshal.md"><strong>user_marshal</strong></a>] verwendet werden. Darüber hinaus können Pipes nicht als Rückgabe Typen verwendet werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2323"></span><span id="midl2323"></span><dl> <dt><strong>MIDL2323</strong></dt> </dl></td>
<td><dl> <dt><span id="feature_requires_the_advanced_interpreted_optimization_option__use_-Oicf"></span><span id="feature_requires_the_advanced_interpreted_optimization_option__use_-oicf"></span><span id="FEATURE_REQUIRES_THE_ADVANCED_INTERPRETED_OPTIMIZATION_OPTION__USE_-OICF"></span>die Funktion erfordert die erweiterte interpretierte Optimierungs Option. use-Oicf</dt> <dd> Dieser Fehler zeigt an, dass der Befehls Zeilenschalter für den <a href="-robust.md"><strong>/robust</strong></a> -Compiler, z. b., den <a href="-oi.md"><strong>/Oicf</strong></a> -Modus erfordert.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2324"></span><span id="midl2324"></span><dl> <dt><strong>MIDL2324</strong></dt> </dl></td>
<td><dl> <dt><span id="feature_requires_the_advanced_interpreted_optimization_option__use_-Oicf"></span><span id="feature_requires_the_advanced_interpreted_optimization_option__use_-oicf"></span><span id="FEATURE_REQUIRES_THE_ADVANCED_INTERPRETED_OPTIMIZATION_OPTION__USE_-OICF"></span>die Funktion erfordert die erweiterte interpretierte Optimierungs Option. use-Oicf</dt> <dd> Diese Warnung <a href="-oi.md"><strong>gibt an,</strong></a> dass für den Befehls Zeilenschalter des <a href="-robust.md"><strong></strong></a> Befehls zeilenbefehls (z. b<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2329"></span><span id="midl2329"></span><dl> <dt><strong>MIDL2329</strong></dt> </dl></td>
<td><dl> <dt><span id="the_optimization_option_is_being_phased_out__use_-Oic"></span><span id="the_optimization_option_is_being_phased_out__use_-oic"></span><span id="THE_OPTIMIZATION_OPTION_IS_BEING_PHASED_OUT__USE_-OIC"></span>die Optimierungs Option wird nach außen eingestellt, Verwendung-OIC</dt> <dd> Der <a href="-oi.md"><strong>/Oi1</strong></a> -Optimierungs Modus wurde in der Mittell-Befehlszeile angegeben. Dieser Modus wird nicht mehr unterstützt, und stattdessen sollte <strong>/Oicf</strong> verwendet werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2330"></span><span id="midl2330"></span><dl> <dt><strong>MIDL2330</strong></dt> </dl></td>
<td><dl> <dt><span id="the_optimization_option_is_being_phased_out__use_-Oicf"></span><span id="the_optimization_option_is_being_phased_out__use_-oicf"></span><span id="THE_OPTIMIZATION_OPTION_IS_BEING_PHASED_OUT__USE_-OICF"></span>die Optimierungs Option wird nach außen eingestellt, use-Oicf</dt> <dd> Der <a href="-oi.md"><strong>/Oi2</strong></a> -Optimierungs Modus wurde in der Mittell-Befehlszeile angegeben. Dieser Modus wird nicht mehr unterstützt, und stattdessen sollte <strong>/Oicf</strong> verwendet werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2331"></span><span id="midl2331"></span><dl> <dt><strong>MIDL2331</strong></dt> </dl></td>
<td><dl> <dt><span id="the_optimization_option_is_being_phased_out__use_-ic"></span><span id="THE_OPTIMIZATION_OPTION_IS_BEING_PHASED_OUT__USE_-IC"></span>die Optimierungs Option wird nach außen eingestellt, Verwendung-IC</dt> <dd> Der I1-Optimierungs Modus wurde in einem [Optimization] ACF-Attribut angegeben. Dieser Modus wird nicht mehr unterstützt, und stattdessen sollte ICF verwendet werden.<br/> Beispiel-ACF-Datei:<br/>
<pre class="syntax" data-space="preserve"><code>[optimize(&quot;i1&quot;)] roo();    //MIDL 2331</code></pre>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2332"></span><span id="midl2332"></span><dl> <dt><strong>MIDL2332</strong></dt> </dl></td>
<td><dl> <dt><span id="the_optimization_option_is_being_phased_out__use_-icf"></span><span id="THE_OPTIMIZATION_OPTION_IS_BEING_PHASED_OUT__USE_-ICF"></span>die Optimierungs Option wird nach außen eingestellt, verwenden Sie "-ICF".</dt> <dd> Der I2-Optimierungs Modus wurde in einem [Optimization] ACF-Attribut angegeben. Dieser Modus wird nicht mehr unterstützt, und stattdessen sollte ICF verwendet werden.<br/> Beispiel-ACF-Datei:<br/>
<pre class="syntax" data-space="preserve"><code>[optimize(&quot;i2&quot;)] roo();    //MIDL 2332</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2333"></span><span id="midl2333"></span><dl> <dt><strong>MIDL2333</strong></dt> </dl></td>
<td><dl> <dt><span id="the_-old_and_-new_switches_are_obsolete__use_-oldtlb_and_-newtlb"></span><span id="THE_-OLD_AND_-NEW_SWITCHES_ARE_OBSOLETE__USE_-OLDTLB_AND_-NEWTLB"></span>der alte und der neue Schalter sind veraltet, verwenden Sie "-oldtlb" und "-newtlb".</dt> <dd> Diese Nachricht ist veraltet und wird nicht mehr von der mittleren l ausgelassen.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2334"></span><span id="midl2334"></span><dl> <dt><strong>MIDL2334</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_argument_value"></span><span id="ILLEGAL_ARGUMENT_VALUE"></span>Ungültiger Argument Wert</dt> <dd> Die zulässigen Varianten des Befehls Zeilenschalters/O umfassen <a href="-os.md"><strong>/OS</strong></a>, <a href="-oi.md"><strong>/Oi</strong></a>, <strong>/OIC</strong>, <strong>/Oicf</strong>und <strong>/OIF</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2335"></span><span id="midl2335"></span><dl> <dt><strong>MIDL2335</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_expression_type_in_constant"></span><span id="ILLEGAL_EXPRESSION_TYPE_IN_CONSTANT"></span>Ungültiger Ausdruckstyp in konstanter</dt> <dd> Der Ausdruck wird nicht zu einer Konstanten ausgewertet.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2336"></span><span id="midl2336"></span><dl> <dt><strong>MIDL2336</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_expression_type_in_enum"></span><span id="ILLEGAL_EXPRESSION_TYPE_IN_ENUM"></span>Ungültiger Ausdruckstyp in Enumeration.</dt> <dd> Ein Enumerationswert in einer Enumerationsdefinition wird nicht <a href="enum.md"><strong>in einen</strong></a> ganzzahligen Typ ausgewertet.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2337"></span><span id="midl2337"></span><dl> <dt><strong>MIDL2337</strong></dt> </dl></td>
<td><dl> <dt><span id="unsatisfied_forward_declaration"></span><span id="UNSATISFIED_FORWARD_DECLARATION"></span>nicht zufrieden gestellte vorwärts Deklaration</dt> <dd> Der mittlerer l-Compiler konnte die Definition einer vorwärts Deklaration nicht auflösen.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2338"></span><span id="midl2338"></span><dl> <dt><strong>MIDL2338</strong></dt> </dl></td>
<td><dl> <dt><span id="switches_are_contradictory"></span><span id="SWITCHES_ARE_CONTRADICTORY"></span>Schalter sind widersprüchlich</dt> <dd> Sie können nicht die Befehls Zeilenschalter <a href="-osf.md"><strong>/OSF</strong></a> und <a href="-ms-ext.md"><strong>/ms_ext</strong></a> verwenden, wenn Sie eine IDL-Datei kompilieren. Sie müssen eine oder die andere auswählen.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2339"></span><span id="midl2339"></span><dl> <dt><strong>MIDL2339</strong></dt> </dl></td>
<td><dl> <dt><span id="MIDL_cannot_generate_HOOKOLE_information_for_the_non-rpc-able_union"></span><span id="midl_cannot_generate_hookole_information_for_the_non-rpc-able_union"></span><span id="MIDL_CANNOT_GENERATE_HOOKOLE_INFORMATION_FOR_THE_NON-RPC-ABLE_UNION"></span>"Mittel l" kann keine "hookole"-Informationen für die nicht-RPC-fähige Union generieren.</dt> <dd> Dieser Fehler ist veraltet. Sie wird ausschließlich aus Gründen der Abwärtskompatibilität bereitgestellt.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2340"></span><span id="midl2340"></span><dl> <dt><strong>MIDL2340</strong></dt> </dl></td>
<td><dl> <dt><span id="no_case_expression_found_for_union"></span><span id="NO_CASE_EXPRESSION_FOUND_FOR_UNION"></span>kein Case-Ausdruck für Union gefunden.</dt> <dd> Jedes Feld einer Union muss eine Case-Anweisung mit einem konstanten Ausdruck enthalten.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2341"></span><span id="midl2341"></span><dl> <dt><strong>MIDL2341</strong></dt> </dl></td>
<td><dl> <dt><span id="_user_marshal__and__wire_marshal__not_supported_with_-Oi_and_-Oic_flags__use_-Os_or_-Oicf"></span><span id="_user_marshal__and__wire_marshal__not_supported_with_-oi_and_-oic_flags__use_-os_or_-oicf"></span><span id="_USER_MARSHAL__AND__WIRE_MARSHAL__NOT_SUPPORTED_WITH_-OI_AND_-OIC_FLAGS__USE_-OS_OR_-OICF"></span>[user_marshal] und [Wire_marshal] werden mit-Oi und-OIC-Flags nicht unterstützt. verwenden Sie "-OS" oder "-Oicf".</dt> <dd> Für die Attribute [<a href="user-marshal.md"><strong>user_marshal</strong></a>] und [<a href="wire-marshal.md"><strong>Wire_marshal</strong></a>] sind die spezifischen Optimierungs Features erforderlich, die nur in <a href="-oi.md"><strong>/Oicf</strong></a> (der nicht über einen Code losen Proxy mit schnellen Format Zeichenfolgen) oder <a href="-os.md"><strong>/OS</strong></a> (Marshalling im gemischten Modus) verfügbar sind.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2342"></span><span id="midl2342"></span><dl> <dt><strong>MIDL2342</strong></dt> </dl></td>
<td><dl> <dt><span id="pipes_can_t_be_used_with_data_serialization__i.e.__encode__and_or__decode_"></span><span id="PIPES_CAN_T_BE_USED_WITH_DATA_SERIALIZATION__I.E.__ENCODE__AND_OR__DECODE_"></span>Pipes können nicht mit Datenserialisierung verwendet werden, d. h. [Encode] und/oder [decodieren]</dt> <dd> Pipes können nicht als Parameter an Prozeduren übergeben werden, die über die Attribute [<a href="encode.md"><strong>Codieren</strong></a>] oder [<a href="decode.md"><strong>decodieren</strong></a>] verfügen.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2343"></span><span id="midl2343"></span><dl> <dt><strong>MIDL2343</strong></dt> </dl></td>
<td><dl> <dt><span id="all_pipe_interface_pointers_must_use_single_indirection"></span><span id="ALL_PIPE_INTERFACE_POINTERS_MUST_USE_SINGLE_INDIRECTION"></span>Alle Pipe-Schnittstellen Zeiger müssen eine einzelne Dereferenzierung verwenden.</dt> <dd> Auf diese Weise ist es nicht möglich, einen Zeiger auf einen Zeiger auf eine Pipe-Schnittstelle zu verwenden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2344"></span><span id="midl2344"></span><dl> <dt><strong>MIDL2344</strong></dt> </dl></td>
<td><dl> <dt><span id="_iid_is____cannot_be_used_with_a_pipe_interface_pointer"></span><span id="_IID_IS____CANNOT_BE_USED_WITH_A_PIPE_INTERFACE_POINTER"></span>[iid_is ()] kann nicht mit einem Pipe-Schnittstellen Zeiger verwendet werden.</dt> <dd> Diese Meldung ist veraltet. Diese Meldung wird vom Compiler nicht mehr verwendet.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2345"></span><span id="midl2345"></span><dl> <dt><strong>MIDL2345</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid_or_inapplicable_-lcid_switch"></span><span id="INVALID_OR_INAPPLICABLE_-LCID_SWITCH"></span>ungültig oder nicht zutreffend-LCID-Schalter</dt> <dd> Der von Ihnen angegebene lokale Bezeichner (LCID) ist ungültig.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2346"></span><span id="midl2346"></span><dl> <dt><strong>MIDL2346</strong></dt> </dl></td>
<td><dl> <dt><span id="the_specified_lcid_is_different_from_previous_specification"></span><span id="THE_SPECIFIED_LCID_IS_DIFFERENT_FROM_PREVIOUS_SPECIFICATION"></span>die angegebene LCID unterscheidet sich von der vorherigen Spezifikation.</dt> <dd> Die in/LCID und [<a href="lcid.md"><strong>LCID</strong></a>] angegebenen Werte unterscheiden sich. Der mittlerer l-Compiler verwendet den letzten definierten.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2347"></span><span id="midl2347"></span><dl> <dt><strong>MIDL2347</strong></dt> </dl></td>
<td><dl> <dt><span id="importlib_is_not_allowed_outside_of_a_library_block"></span><span id="IMPORTLIB_IS_NOT_ALLOWED_OUTSIDE_OF_A_LIBRARY_BLOCK"></span>importlib ist außerhalb eines Bibliotheks Blocks nicht zulässig.</dt> <dd> Alle [<a href="importlib.md"><strong>importlib</strong></a>]-Anweisungen sollten in einem [<a href="library.md"><strong>Library</strong></a>]-Block auftreten.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2348"></span><span id="midl2348"></span><dl> <dt><strong>MIDL2348</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid_floating_point_value"></span><span id="INVALID_FLOATING_POINT_VALUE"></span>Ungültiger Gleit Komma Wert.</dt> <dd> Dieser Fehler sollte nicht von der Mittell ausgegeben werden. Wenn dieser Fehler angezeigt wird, melden Sie Microsoft einen Fehler, der alle Dateien bereitstellt, die zum Reproduzieren des Fehlers erforderlich sind, einschließlich ihrer IDL-Dateien, ACF-Dateien, Header usw.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2349"></span><span id="midl2349"></span><dl> <dt><strong>MIDL2349</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid_member"></span><span id="INVALID_MEMBER"></span>Ungültiger Member</dt> <dd> Prozeduren können nicht Mitglieder einer-Bibliothek sein.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2350"></span><span id="midl2350"></span><dl> <dt><strong>MIDL2350</strong></dt> </dl></td>
<td><dl> <dt><span id="possible_invalid_member"></span><span id="POSSIBLE_INVALID_MEMBER"></span>möglicher Ungültiger Member</dt> <dd> Um ein gültiges Member einer Bibliothek zu sein, muss das Library-Element ein Modul, eine dispinterface, eine Co-Klasse, eine if-Anweisung, eine Struktur, eine Union, eine Enumeration oder eine vorwärts Deklaration sein.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2351"></span><span id="midl2351"></span><dl> <dt><strong>MIDL2351</strong></dt> </dl></td>
<td><dl> <dt><span id="mismatch_in_pipe_and_interface_types"></span><span id="MISMATCH_IN_PIPE_AND_INTERFACE_TYPES"></span>nicht übereinstimmende Pipe-und Schnittstellentypen</dt> <dd> Diese Meldung ist veraltet.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2352"></span><span id="midl2352"></span><dl> <dt><strong>MIDL2352</strong></dt> </dl></td>
<td><dl> <dt><span id="string__varying_array__conformant_array_and_full_pointer_parameters_may_be_incompatible_with_pipe_parameters_during_run_time"></span><span id="STRING__VARYING_ARRAY__CONFORMANT_ARRAY_AND_FULL_POINTER_PARAMETERS_MAY_BE_INCOMPATIBLE_WITH_PIPE_PARAMETERS_DURING_RUN_TIME"></span>Zeichen folgen-, unterschiedliche Array-, konforme Array-und voll Zeiger Parameter können während der Laufzeit nicht mit Pipe-Parametern kompatibel sein.</dt> <dd> Eine Methode, die eine oder mehrere [in]-Zeichen folgen, unterschiedliche Arrays, konforme Arrays und vollständige Zeiger Parameter und any [in] Pipe-Parameter kombiniert, führt zur Generierung eines Stubs, der nur auf <strong>ncacn_ *</strong> -und <a href="ncalrpc.md"><strong>Ncalrpc</strong></a> -Protokoll Sequenzen auf Windows-Computern ausgeführt wird. Wenn Sie den Stub zum Aufrufen von <strong>ncadg_ *</strong> -Protokoll Sequenzen oder zum Akzeptieren von Aufrufen von anderen OSF-DCE-RPC-Anbietern verwenden, können während der Laufzeit Fehler auf dem Server generiert werden. Dieser Fehler tritt ab Windows Server 2003 auf.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2353"></span><span id="midl2353"></span><dl> <dt><strong>MIDL2353</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_must_be_in"></span><span id="PARAMETER_MUST_BE_IN"></span>der Parameter muss sich in befinden.</dt> <dd> Asynchrone Handles müssen [<a href="in.md"><strong>in</strong></a>]-Parameter sein.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2354"></span><span id="midl2354"></span><dl> <dt><strong>MIDL2354</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_type_of_an__async__object_must_be_a_double_pointer_to_an_interface"></span><span id="PARAMETER_TYPE_OF_AN__ASYNC__OBJECT_MUST_BE_A_DOUBLE_POINTER_TO_AN_INTERFACE"></span>der Parametertyp eines [Async]-Objekts muss ein doppelter Zeiger auf eine Schnittstelle sein.</dt> <dd> Der-Parameter muss vom Typ <strong>iasyncmanager</strong> * * sein.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2355"></span><span id="midl2355"></span><dl> <dt><strong>MIDL2355</strong></dt> </dl></td>
<td><dl> <dt><span id="incorrect_async_handle_type"></span><span id="INCORRECT_ASYNC_HANDLE_TYPE"></span>falscher Async-Handlertyp.</dt> <dd> Der Handlertyp muss <strong>iasyncmanager</strong> oder ein von <strong>iasyncmanager</strong>abgeleiteter Typ sein.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2356"></span><span id="midl2356"></span><dl> <dt><strong>MIDL2356</strong></dt> </dl></td>
<td><dl> <dt><span id="the__internal__switch_enables_unsupported_features__use_with_caution"></span><span id="THE__INTERNAL__SWITCH_ENABLES_UNSUPPORTED_FEATURES__USE_WITH_CAUTION"></span>der &quot; interne &quot; Switch ermöglicht nicht unterstützte Funktionen, Verwendung mit Vorsicht.</dt> <dd> Vermeiden Sie die Verwendung dieses Schalters.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2357"></span><span id="midl2357"></span><dl> <dt><strong>MIDL2357</strong></dt> </dl></td>
<td><dl> <dt><span id="async_procedures_cannot_use_auto_handle"></span><span id="ASYNC_PROCEDURES_CANNOT_USE_AUTO_HANDLE"></span>Async-Prozeduren können kein automatisches Handle verwenden</dt> <dd> Prozeduren mit dem Attribut [<a href="async.md"><strong>Async</strong></a>] erfordern explizite Handles.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2358"></span><span id="midl2358"></span><dl> <dt><strong>MIDL2358</strong></dt> </dl></td>
<td><dl> <dt><span id="error_status_t_should_have_both__comm_status__and__fault_status_"></span><span id="ERROR_STATUS_T_SHOULD_HAVE_BOTH__COMM_STATUS__AND__FAULT_STATUS_"></span>error_status_t sollten sowohl [comm_status] als auch [fault_status] aufweisen.</dt> <dd> Eine Prozedur wurde mit den IDL-Attributen [vielleicht] oder [Message] angegeben, aber der Rückgabetyp verfügt nur über die ACF-Attribute [comm_status] oder [fault_status]. Beide ACF-Attribute sind erforderlich.<br/> Beispiel-ACF-Datei:<br/>
<pre class="syntax" data-space="preserve"><code>[comm_status] roo();    //MIDL 2358
[fault_status] bar();    //MIDL 2358
[comm_status, fault_status] baz();    //OK</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2359"></span><span id="midl2359"></span><dl> <dt><strong>MIDL2359</strong></dt> </dl></td>
<td><dl> <dt><span id="this_construct_is_only_allowed_within_a_library_block"></span><span id="THIS_CONSTRUCT_IS_ONLY_ALLOWED_WITHIN_A_LIBRARY_BLOCK"></span>Dieses Konstrukt ist nur innerhalb eines Bibliotheks Blocks zulässig.</dt> <dd> Ein Modul kann nur innerhalb eines Bibliotheks Blocks auftreten.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2360"></span><span id="midl2360"></span><dl> <dt><strong>MIDL2360</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid_type_redefinition"></span><span id="INVALID_TYPE_REDEFINITION"></span>Ungültige Typneudefinition.</dt> <dd> Ein neuer Typ wurde rekursiv für einen nicht vorhandenen Typ definiert.<br/> Beispiel:<br/>
<pre class="syntax" data-space="preserve"><code>typedef roo roo[10];    //MIDL 2360</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2361"></span><span id="midl2361"></span><dl> <dt><strong>MIDL2361</strong></dt> </dl></td>
<td><dl> <dt><span id="procedures_with_a__vararg__attribute_must_have_a_SAFEARRAY_VARIANT__parameter__param_order_is__vararg____lcid____retval_"></span><span id="procedures_with_a__vararg__attribute_must_have_a_safearray_variant__parameter__param_order_is__vararg____lcid____retval_"></span><span id="PROCEDURES_WITH_A__VARARG__ATTRIBUTE_MUST_HAVE_A_SAFEARRAY_VARIANT__PARAMETER__PARAM_ORDER_IS__VARARG____LCID____RETVAL_"></span>Prozeduren mit einem [vararg]-Attribut müssen einen SAFEARRAY-Parameter (Variant) aufweisen; die param-Reihenfolge ist [vararg], [LCID], [retval].</dt> <dd> Die meisten Parameter für Prozeduren mit dem [<a href="vararg.md"><strong>vararg</strong></a>]-Attribut müssen vor dem <strong>SAFEARRAY-Parameter (Variant)</strong> vorkommen. Der <strong>SAFEARRAY-Parameter (Variant)</strong> muss vorhanden sein. Wenn die Parameterliste einen Parameter mit dem [ <a href="lcid.md"><strong>LCID</strong></a>]-Attribut enthält, muss Sie dem <strong>SAFEARRAY-Parameter (Variant)</strong> folgen. Wenn die Parameterliste einen Parameter mit dem [<a href="retval.md"><strong>retval</strong></a>]-Attribut enthält, muss Sie nach dem-Parameter mit dem [<strong>LCID</strong>]-Attribut auftreten.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2363"></span><span id="midl2363"></span><dl> <dt><strong>MIDL2363</strong></dt> </dl></td>
<td><dl> <dt><span id="too_many_methods_in_the_interface__requires_Windows_2000_or_greater"></span><span id="too_many_methods_in_the_interface__requires_windows_2000_or_greater"></span><span id="TOO_MANY_METHODS_IN_THE_INTERFACE__REQUIRES_WINDOWS_2000_OR_GREATER"></span>zu viele Methoden in der Schnittstelle, erfordert Windows 2000 oder höher.</dt> <dd> Der mittlerer l-Compiler lässt bei der Kompilierung im <a href="-oi.md"><strong>/Oicf</strong></a> -Modus nicht mehr als 1024 Methoden in einer Schnittstelle zu.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2364"></span><span id="midl2364"></span><dl> <dt><strong>MIDL2364</strong></dt> </dl></td>
<td><dl> <dt><span id="switch_is_being_phased_out"></span><span id="SWITCH_IS_BEING_PHASED_OUT"></span>der Switch wird nach außen eingestellt.</dt> <dd> Die folgenden Schalter sind veraltet:/<strong>hookole</strong>,/<strong>einv Win16</strong>und/in<strong>.</strong><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2365"></span><span id="midl2365"></span><dl> <dt><strong>MIDL2365</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_derive_from_IAdviseSink__IAdviseSink2__or_IAdviseSinkEx"></span><span id="cannot_derive_from_iadvisesink__iadvisesink2__or_iadvisesinkex"></span><span id="CANNOT_DERIVE_FROM_IADVISESINK__IADVISESINK2__OR_IADVISESINKEX"></span>Ableiten von IAdviseSink, IAdviseSink2 oder iadvisesinkex nicht möglich.</dt> <dd> Diese Schnittstellen können nicht erweitert werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2366"></span><span id="midl2366"></span><dl> <dt><strong>MIDL2366</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_assign_a_default_value"></span><span id="CANNOT_ASSIGN_A_DEFAULT_VALUE"></span>ein Standardwert kann nicht zugewiesen werden.</dt> <dd> Das Zuweisen eines Standardwerts zu einem Parameter ist in Visual Basic zulässig, jedoch nicht in C++. Wenn Sie C++ verwenden, wird der Standardwert ignoriert.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2367"></span><span id="midl2367"></span><dl> <dt><strong>MIDL2367</strong></dt> </dl></td>
<td><dl> <dt><span id="type_library_generation_for_DOS_Win16_MAC_is_not_supported"></span><span id="type_library_generation_for_dos_win16_mac_is_not_supported"></span><span id="TYPE_LIBRARY_GENERATION_FOR_DOS_WIN16_MAC_IS_NOT_SUPPORTED"></span>die Generierung der Typbibliothek für DOS/Win16/Mac wird nicht unterstützt.</dt> <dd> In der Mitte werden 16-Bit-Typbibliotheken nicht unterstützt.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2368"></span><span id="midl2368"></span><dl> <dt><strong>MIDL2368</strong></dt> </dl></td>
<td><dl> <dt><span id="error_generating_type_library__ignored"></span><span id="ERROR_GENERATING_TYPE_LIBRARY__IGNORED"></span>Fehler beim Erzeugen der Typbibliothek, wird ignoriert.</dt> <dd> Beim Erstellen der Typbibliothek ist ein nicht schwerwiegender Fehler aufgetreten.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2369"></span><span id="midl2369"></span><dl> <dt><strong>MIDL2369</strong></dt> </dl></td>
<td><dl> <dt><span id="exceeded_stack_size_for__Oi__using__Os"></span><span id="exceeded_stack_size_for__oi__using__os"></span><span id="EXCEEDED_STACK_SIZE_FOR__OI__USING__OS"></span>Überschreiten der Stapelgröße für/Oi mit/OS</dt> <dd> Der Optimierungs Modus "-Oi" ist auf 128 Bytes Stapel Speicherplatz für Parameter beschränkt. Der Compiler hat automatisch in den Optimierungs Modus des Betriebssystems gewechselt, um diese Einschränkung zu umgehen.<br/> Um diese Warnung zu vermeiden, verwenden Sie die Optimierungs Modi-Oicf oder-OS. Der Optimierungs Modus kann in der Befehlszeile geändert werden, indem Sie "-Oicf" oder "-OS" anstelle von "-Oi" angeben oder indem &quot; &quot; &quot; &quot; Sie der Funktion in der ACF-Datei ein [optimize9 ICF]]-Attribut oder ein-Optimierungs Attribut [(s)] hinzufügen.<br/> Diese Warnung tritt normalerweise auf, wenn große Strukturen als Parameter nach Wert übergeben werden. Die erforderliche Stapelgröße kann durch Übergeben eines Zeigers auf die-Struktur gesenkt werden.<br/> Beispiel:<br/>
<pre class="syntax" data-space="preserve"><code>typedef struct
{
char a[127];
}
large;
//This function has a stack size of 132 (x86) or 136 (alpha) on 32-bit systems
void roo(large s, int a);    //MIDL 2360
// workaround: pass by reference
void bar (large *s, int a);</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2370"></span><span id="midl2370"></span><dl> <dt><strong>MIDL2370</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of__robust_requires__Oicf__switching_modes"></span><span id="use_of__robust_requires__oicf__switching_modes"></span><span id="USE_OF__ROBUST_REQUIRES__OICF__SWITCHING_MODES"></span>die Verwendung von/robust erfordert/Oicf, Wechsel Modi</dt> <dd> Sie müssen den <a href="-oi.md"><strong>/Oicf</strong></a> -Modus kompilieren, wenn Sie den <a href="-robust.md"><strong>/robust</strong></a> -Schalter in der Befehlszeile angeben.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2371"></span><span id="midl2371"></span><dl> <dt><strong>MIDL2371</strong></dt> </dl></td>
<td><dl> <dt><span id="incorrect_range_specified"></span><span id="INCORRECT_RANGE_SPECIFIED"></span>falscher Bereich angegeben.</dt> <dd> Der höchste Wert, der in einem [<a href="range.md"><strong>Range</strong></a>]-Attribut angegeben ist, ist kleiner als der niedrigste Wert.<br/> Beispiel:<br/>
<pre class="syntax" data-space="preserve"><code>void roo([range(3,2)] int a);    //MIDL 2371</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2372"></span><span id="midl2372"></span><dl> <dt><strong>MIDL2372</strong></dt> </dl></td>
<td><dl> <dt><span id="_invalid_combination_of__in__only_and__out__parameters_for__async_uuid__interface"></span><span id="_INVALID_COMBINATION_OF__IN__ONLY_AND__OUT__PARAMETERS_FOR__ASYNC_UUID__INTERFACE"></span> Ungültige Kombination von [in]-und [out]-Parametern für [Async_uuid]-Schnittstelle.</dt> <dd> Für diese Art von Schnittstelle sind nur einfache Kombinationen von Attributen mit [<a href="in.md"><strong>in</strong></a>]-oder [<a href="out-idl.md"><strong>out</strong></a>]-Parametern zulässig.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2373"></span><span id="midl2373"></span><dl> <dt><strong>MIDL2373</strong></dt> </dl></td>
<td><dl> <dt><span id="DOS__Win16_and_MAC_platforms_are_not_supported_with__robust"></span><span id="dos__win16_and_mac_platforms_are_not_supported_with__robust"></span><span id="DOS__WIN16_AND_MAC_PLATFORMS_ARE_NOT_SUPPORTED_WITH__ROBUST"></span>DOS-, Win16-und Mac-Plattformen werden bei/robust nicht unterstützt</dt> <dd> Die/robust-Option unterstützt die Option " <a href="-robust.md"><strong></strong></a> " unter Microsoft Windows 2000 oder höher.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2374"></span><span id="midl2374"></span><dl> <dt><strong>MIDL2374</strong></dt> </dl></td>
<td><dl> <dt><span id="support_for_NT_3.51_style_stubless_proxies_for_object_interfaces_will_be_phased_out__use__Oif."></span><span id="support_for_nt_3.51_style_stubless_proxies_for_object_interfaces_will_be_phased_out__use__oif."></span><span id="SUPPORT_FOR_NT_3.51_STYLE_STUBLESS_PROXIES_FOR_OBJECT_INTERFACES_WILL_BE_PHASED_OUT__USE__OIF."></span>die Unterstützung für nicht-Unterstützung für die Proxys des NT-3,51-Stils für Objekt Schnittstellen wird /OIF. verwenden</dt> <dd> Dieser Modus ist veraltet. Verwenden Sie <a href="-oi.md"><strong>/OIF</strong></a> oder <strong>/Oicf</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2375"></span><span id="midl2375"></span><dl> <dt><strong>MIDL2375</strong></dt> </dl></td>
<td><dl> <dt><span id="_encode__or__decode__with__robust_requires__Oicf"></span><span id="_encode__or__decode__with__robust_requires__oicf"></span><span id="_ENCODE__OR__DECODE__WITH__ROBUST_REQUIRES__OICF"></span>[codieren] oder [Decode] mit/robust erfordert/Oicf</dt> <dd> Die Serialisierung kann nicht ausgeführt werden, wenn der <a href="-robust.md"><strong>/robust</strong></a> -Schalter angegeben wird.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2377"></span><span id="midl2377"></span><dl> <dt><strong>MIDL2377</strong></dt> </dl></td>
<td><dl> <dt><span id="conflicting_attributes_specified"></span><span id="CONFLICTING_ATTRIBUTES_SPECIFIED"></span>in Konflikt stehende Attribute angegeben</dt> <dd> Es wurden sowohl [<a href="context-handle-serialize.md"><strong>context_handle_serialize</strong></a>] als auch [<a href="context-handle-noserialize.md"><strong>context_handle_noserialize</strong></a>] angegeben.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2378"></span><span id="midl2378"></span><dl> <dt><strong>MIDL2378</strong></dt> </dl></td>
<td><dl> <dt><span id="_serialize____noserialize__can_be_applied_to_context_handles"></span><span id="_SERIALIZE____NOSERIALIZE__CAN_BE_APPLIED_TO_CONTEXT_HANDLES"></span>[Serialize], [noserialize] kann auf context_handles angewendet werden.</dt> <dd> Die ACF-Attribute [context_handle_serialize] oder [context_handle_noserialize] können nur auf Typen angewendet werden, bei denen es sich um Kontext Handles handelt.<br/> Beispiel für eine IDL-Datei:<br/>
<pre class="syntax" data-space="preserve"><code>typedef /*[context_handle] */ void *PV;    //Note: PV is *not* a context handle.</code></pre>
Beispiel-ACF-Datei:<br/>
<pre class="syntax" data-space="preserve"><code>typedef [context_handle_serialize] PV;    //MIDL 2378</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2379"></span><span id="midl2379"></span><dl> <dt><strong>MIDL2379</strong></dt> </dl></td>
<td><dl> <dt><span id="The_compiler_reached_a_limit_for_a_format_string_representation._See_documentation_for_advice."></span><span id="the_compiler_reached_a_limit_for_a_format_string_representation._see_documentation_for_advice."></span><span id="THE_COMPILER_REACHED_A_LIMIT_FOR_A_FORMAT_STRING_REPRESENTATION._SEE_DOCUMENTATION_FOR_ADVICE."></span>Der Compiler hat eine Beschränkung für eine Formatzeichen folgen Darstellung erreicht. Weitere Informationen finden Sie in der Dokumentation.</dt> <dd> Der mittlerer l-Compiler hat eine Beschränkung von 64 KB für Format Zeichenfolgen. Dieser Fehler tritt im Allgemeinen auf, wenn IDL-Dateien andere IDL-Dateien enthalten. Die zusammengesetzte IDL-Datei, die von allen include-Anweisungen generiert wird, überschreitet die Grenzwerte der typdarstellungs Tabellen des marshallingtriebwerk-interpreters. Verwenden Sie die Import-Direktive anstelle der include-Direktive in ihren IDL-Dateien. Weitere Informationen finden Sie unter <a href="importing-system-header-files.md">Importieren von System Header Dateien</a>, <a href="include.md"><strong>einschließen</strong></a>und <a href="import.md"><strong>importieren</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2380"></span><span id="midl2380"></span><dl> <dt><strong>MIDL2380</strong></dt> </dl></td>
<td><dl> <dt><span id="wire_format_may_be_incorrect__you_may_need_to_use_-ms_conf_struct__see_documentation_for_advice"></span><span id="WIRE_FORMAT_MAY_BE_INCORRECT__YOU_MAY_NEED_TO_USE_-MS_CONF_STRUCT__SEE_DOCUMENTATION_FOR_ADVICE"></span>das Wire-Format ist möglicherweise falsch. möglicherweise müssen Sie-ms_conf_struct verwenden, und in der Dokumentation finden Sie Ratschläge.</dt> <dd> Der mittlerer l-Compiler konnte kein übertragbarer Format für die Daten generieren. Eine gängige Methode, diesen Fehler zu erhalten, besteht darin, eine <strong>ms_conf_struct</strong> in einer komplexen Struktur zu definieren.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2381"></span><span id="midl2381"></span><dl> <dt><strong>MIDL2381</strong></dt> </dl></td>
<td><dl> <dt><span id="a_stack_size_or_an_offset_bigger_than_64_K_limit._See_documentation_for_advice."></span><span id="a_stack_size_or_an_offset_bigger_than_64_k_limit._see_documentation_for_advice."></span><span id="A_STACK_SIZE_OR_AN_OFFSET_BIGGER_THAN_64_K_LIMIT._SEE_DOCUMENTATION_FOR_ADVICE."></span>eine Stapelgröße oder ein Offset, der größer als 64 K ist. Weitere Informationen finden Sie in der Dokumentation.</dt> <dd> Der-Befehl führt zu einem Stapel, der größer als 64 KB ist. Versuchen Sie, die Daten in kleineren Blöcken zu übergeben.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2382"></span><span id="midl2382"></span><dl> <dt><strong>MIDL2382</strong></dt> </dl></td>
<td><dl> <dt><span id="an_interpreter_mode_forced_for_64-bit_platform_"></span><span id="AN_INTERPRETER_MODE_FORCED_FOR_64-BIT_PLATFORM_"></span>ein für die 64-Bit-Plattform erzwungener Interpretermodus. </dt> <dd> 64-Bit-Plattformen erfordern den/Oicf-Kompilierungs Modus.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2383"></span><span id="midl2383"></span><dl> <dt><strong>MIDL2383</strong></dt> </dl></td>
<td><dl> <dt><span id="The_array_element_size_is_bigger_than_64_KB_limit."></span><span id="the_array_element_size_is_bigger_than_64_kb_limit."></span><span id="THE_ARRAY_ELEMENT_SIZE_IS_BIGGER_THAN_64_KB_LIMIT."></span>Die Array Elementgröße ist größer als 64 KB.</dt> <dd> Alle Array Elemente müssen eine Größe von weniger als 64 KB aufweisen.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2384"></span><span id="midl2384"></span><dl> <dt><strong>MIDL2384</strong></dt> </dl></td>
<td><dl> <dt><span id="there_can_be_only_one__Icid__parameter_in_a_method__and_it_should_be_last_or_second_to_last_if_last_parameter_has__retval_"></span><span id="there_can_be_only_one__icid__parameter_in_a_method__and_it_should_be_last_or_second_to_last_if_last_parameter_has__retval_"></span><span id="THERE_CAN_BE_ONLY_ONE__ICID__PARAMETER_IN_A_METHOD__AND_IT_SHOULD_BE_LAST_OR_SECOND_TO_LAST_IF_LAST_PARAMETER_HAS__RETVAL_"></span>Es darf nur ein [ICID]-Parameter in einer Methode vorhanden sein, und es muss der letzte oder zweite Wert sein, wenn der letzte Parameter [retval] hat.</dt> <dd> Ein Parameter mit dem [<a href="lcid.md"><strong>LCID</strong></a>]-Attribut muss zuletzt auftreten. Die einzige Ausnahme besteht darin, dass es auch einen Parameter mit dem Attribut [<a href="retval.md"><strong>retval</strong></a>] gibt. Wenn beide vorkommen, muss das zweite für den letzten Parameter in der Parameterliste über das [ <strong>LCID</strong>]-Attribut verfügen. Der letzte Parameter muss das [<strong>retval</strong>]-Attribut aufweisen.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2385"></span><span id="midl2385"></span><dl> <dt><strong>MIDL2385</strong></dt> </dl></td>
<td><dl> <dt><span id="incorrect_syntax_for_midl_pragma"></span><span id="INCORRECT_SYNTAX_FOR_MIDL_PRAGMA"></span>falsche Syntax für midl_pragma</dt> <dd> Der mittlerer l-Compiler hat einen unbekannten Syntax Fehler in einer midl_pragma-Anweisung erkannt.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2386"></span><span id="midl2386"></span><dl> <dt><strong>MIDL2386</strong></dt> </dl></td>
<td><dl> <dt><span id="__int3264_is_not_supported_in__osf_mode"></span><span id="__INT3264_IS_NOT_SUPPORTED_IN__OSF_MODE"></span>__int3264 wird im/OSF-Modus nicht unterstützt.</dt> <dd> Wenn Sie __int3264 verwenden müssen, kompilieren Sie im/MS-ext-Modus.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2387"></span><span id="midl2387"></span><dl> <dt><strong>MIDL2387</strong></dt> </dl></td>
<td><dl> <dt><span id="unresolved_symbol_in_type_library"></span><span id="UNRESOLVED_SYMBOL_IN_TYPE_LIBRARY"></span>nicht aufgelöstes Symbol in Typbibliothek</dt> <dd> Der Compiler konnte eine formale Deklaration oder einen referenzierten Typ in der Typbibliothek nicht auflösen.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2388"></span><span id="midl2388"></span><dl> <dt><strong>MIDL2388</strong></dt> </dl></td>
<td><dl> <dt><span id="async_pipes_cannot_be_passed_by_value"></span><span id="ASYNC_PIPES_CANNOT_BE_PASSED_BY_VALUE"></span>Async-Pipes können nicht als Wert übermittelt werden.</dt> <dd> Asynchrone Pipes sollten als Verweis oder als Adresse übermittelt werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2389"></span><span id="midl2389"></span><dl> <dt><strong>MIDL2389</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_offset_exceed_64-KB_limit_for_interpreted_procedures"></span><span id="parameter_offset_exceed_64-kb_limit_for_interpreted_procedures"></span><span id="PARAMETER_OFFSET_EXCEED_64-KB_LIMIT_FOR_INTERPRETED_PROCEDURES"></span>Parameter Offset überschreitet den Grenzwert von 64 KB für interpretierte Prozeduren</dt> <dd> Dieser Fehler bedeutet in der Regel, dass eine Prozedur zu viele Parameter aufweist.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2390"></span><span id="midl2390"></span><dl> <dt><strong>MIDL2390</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid_array_element"></span><span id="INVALID_ARRAY_ELEMENT"></span>ungültiges Array Element.</dt> <dd> Pipes können nicht als Array Elemente verwendet werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2391"></span><span id="midl2391"></span><dl> <dt><strong>MIDL2391</strong></dt> </dl></td>
<td><dl> <dt><span id="dispinterface_members_must_be_methods__properties_or_interfaces"></span><span id="DISPINTERFACE_MEMBERS_MUST_BE_METHODS__PROPERTIES_OR_INTERFACES"></span>dispinterface-Member müssen Methoden, Eigenschaften oder Schnittstellen sein.</dt> <dd> Eine dispinterface kann keine Typdefinitionen, Strukturen, Enumerationen oder Unions enthalten.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2392"></span><span id="midl2392"></span><dl> <dt><strong>MIDL2392</strong></dt> </dl></td>
<td><dl> <dt><span id="_local__procedure_without__call_as_"></span><span id="_LOCAL__PROCEDURE_WITHOUT__CALL_AS_"></span>[local] Prozedur ohne [Call_as]</dt> <dd> Objekt Prozeduren, die über das [<a href="local.md"><strong>local</strong></a>]-Attribut verfügen, benötigen auch das [<a href="call-as.md"><strong>Call_as</strong></a>]-Attribut.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2393"></span><span id="midl2393"></span><dl> <dt><strong>MIDL2393</strong></dt> </dl></td>
<td><dl> <dt><span id="multi_dimensional_vector__switching_to__Oicf"></span><span id="multi_dimensional_vector__switching_to__oicf"></span><span id="MULTI_DIMENSIONAL_VECTOR__SWITCHING_TO__OICF"></span>mehrdimensionaler Vektor, Wechsel zu/Oicf</dt> <dd> Der <a href="-os.md"><strong>/OS</strong></a> -Optimierungs Modus unterstützt keine Arrays mit mehrdimensionalen, nicht fester Größe. Der Compiler hat für diese Funktion den Optimierungs Modus automatisch auf/<strong>Oicf</strong> umgestellt. <br/> Diese Warnung kann Global unterdrückt werden, indem der Compilermodus durch Angeben von/<strong>Oicf</strong> in der Mittell-Befehlszeile oder durch die Verwendung <strong>midl_pragma</strong> Warnung (deaktivieren: 2393) in der IDL-Datei geändert wird. Der Optimierungs Modus kann für eine einzelne Funktion geändert werden, indem das Attribut [<strong>optimieren ( &quot; ICF &quot; )</strong>] der Funktion in der ACF-Datei hinzugefügt wird.<br/> Das folgende Beispiel veranschaulicht diese Warnung:<br/>
<pre class="syntax" data-space="preserve"><code>void roo(long s1, [size_is(s1)] long a[][30];    //MIDL2393
void bar(long s1, long s2, [size_is(s1,s2) long **a);//MIDL2393</code></pre>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2395"></span><span id="midl2395"></span><dl> <dt><strong>MIDL2395</strong></dt> </dl></td>
<td><dl> <dt><span id="type_or_construct_not_supported_in_a_library_block_because_Oleaut32.dll_support_for_64-KB_polymorphic_types_is_missing"></span><span id="type_or_construct_not_supported_in_a_library_block_because_oleaut32.dll_support_for_64-kb_polymorphic_types_is_missing"></span><span id="TYPE_OR_CONSTRUCT_NOT_SUPPORTED_IN_A_LIBRARY_BLOCK_BECAUSE_OLEAUT32.DLL_SUPPORT_FOR_64-KB_POLYMORPHIC_TYPES_IS_MISSING"></span>der Typ oder das Konstrukt wird in einem Bibliotheks Block nicht unterstützt, da Oleaut32.dll Unterstützung für polymorphe Typen mit 64 KB fehlt.</dt> <dd> Die OLE-Automatisierung unterstützt keine polymorphen Typen (z. b. _int3264, INT_PTR usw.). Diese Typen weisen nicht kompatible Daten Darstellungen zwischen 32-Bit-und 64-Bit-Plattformen auf. Der Remote Aufruf schlägt zur Laufzeit auf 64-Bit-Plattformen fehl.<br/>
<blockquote>
[!Note]<br />
Beachten Sie, dass ab Windows 2000-Version 64-Bit-TLB-Dateien von der OLE-Automatisierung unterstützt werden, indem 32-Bit-TLB-Informationen zur Laufzeit von umgerechnet werden. Daher wird nur die 32-Bit-TLB-Generierung von der mittleren l unterstützt.
</blockquote>
<br/> Wenn die-Klasse nur zum Generieren einer Header Datei verwendet wird, unterdrückt der <a href="-notlb.md"><strong>/notlb</strong></a> -Schalter die Generierung der TLB-Datei.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2396"></span><span id="midl2396"></span><dl> <dt><strong>MIDL2396</strong></dt> </dl></td>
<td><dl> <dt><span id="old_interpreter_code_being_generated_for_64b"></span><span id="OLD_INTERPRETER_CODE_BEING_GENERATED_FOR_64B"></span>der alte interpretercode wird für 64b generiert.</dt> <dd> Dieser Fehler ist veraltet. Wenn dieser Fehler angezeigt wird, melden Sie einen Fehler an Microsoft, und geben Sie Ihre IDL-Dateien, ACF-Dateien und die vollständige Mittell-Befehlszeile an.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2397"></span><span id="midl2397"></span><dl> <dt><strong>MIDL2397</strong></dt> </dl></td>
<td><dl> <dt><span id="the_compiler_switch_is_not_supported_anymore"></span><span id="THE_COMPILER_SWITCH_IS_NOT_SUPPORTED_ANYMORE"></span>der Compilerschalter wird nicht mehr unterstützt.</dt> <dd> Die angegebenen Switches werden nicht mehr unterstützt.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2398"></span><span id="midl2398"></span><dl> <dt><strong>MIDL2398</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_execute_MIDL_engine"></span><span id="cannot_execute_midl_engine"></span><span id="CANNOT_EXECUTE_MIDL_ENGINE"></span>die mittlere Engine kann nicht ausgeführt werden.</dt> <dd> Ab der Windows 2000-Version (mittlerer l-Version 5.03.279) wird der Mittelwert Compiler mithilfe von zwei ausführbaren Dateien implementiert: Midl.exe (Treiber) und Midlc.exe (die Compiler-Engine). Dieser Fehler zeigt an, dass der Midl.exe Midlc.exe nicht starten kann. Stellen Sie sicher, dass sich Midlc.exe im gleichen Verzeichnis wie Midl.exe befindet und dass Sie die gleiche Version haben.<br/> Der Fehler ist möglicherweise darauf zurückzuführen, dass Midl.exe kopiert, jedoch nicht aus der letzten Verteilung Midlx.exe. Führen Sie in der Befehlszeile die Dateien " <strong>Mittel l</strong> " und/oder " <strong>mittellc</strong> " ohne Parameter aus, um die Versionsnummer der ausführbaren Datei anzuzeigen.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2399"></span><span id="midl2399"></span><dl> <dt><strong>MIDL2399</strong></dt> </dl></td>
<td><dl> <dt><span id="bad_commands_from_driver"></span><span id="BAD_COMMANDS_FROM_DRIVER"></span>Ungültige Befehle vom Treiber.</dt> <dd> Ab der Windows 2000-Version (mittlerer l-Version 5.03.279) wird der Mittelwert Compiler mithilfe von zwei ausführbaren Dateien implementiert: Midl.exe (Treiber) und Midlc.exe (die Compiler-Engine). Dieser Fehler zeigt an, dass die temporäre Datei, die zum Übergeben von Befehlen von Midl.exe an Midlc.exe verwendet wird, nicht vorhanden oder beschädigt ist. Stellen Sie sicher, dass sich Midlc.exe im gleichen Verzeichnis wie Midl.exe befindet und dass Sie die gleiche Version haben.<br/> Der Fehler wurde möglicherweise durch den Versuch verursacht, Midlc.exe direkt oder durch Kopieren Midl.exe, aber nicht von der letzten Verteilung Midlc.exe auszuführen. Führen Sie in der Befehlszeile die Dateien " <strong>Mittel l</strong> " und/oder " <strong>mittellc</strong> " ohne Parameter aus, um die Versionsnummer der ausführbaren Datei anzuzeigen.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2400"></span><span id="midl2400"></span><dl> <dt><strong>MIDL2400</strong></dt> </dl></td>
<td><dl> <dt><span id="for_ole_automation__optional_parameters_should_be_VARIANT_or_VARIANT__"></span><span id="for_ole_automation__optional_parameters_should_be_variant_or_variant__"></span><span id="FOR_OLE_AUTOMATION__OPTIONAL_PARAMETERS_SHOULD_BE_VARIANT_OR_VARIANT__"></span>bei der OLE-Automatisierung sollten optionale Parameter Variant oder Variant lauten *</dt> <dd> Für OLE-Automatisierung müssen alle [optional]-Parameter vom Typ <strong>Variant</strong> oder <strong>Variant *</strong>sein.<br/> Bei der OLE-Automatisierung kann die Verwendung von nicht-Variant-Parametern bewirken, dass der Aufruf zur Laufzeit fehlschlägt oder nicht definierte Daten für die [<a href="optional.md"><strong>optional</strong></a>]-Parameter übergeben werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2401"></span><span id="midl2401"></span><dl> <dt><strong>MIDL2401</strong></dt> </dl></td>
<td><dl> <dt><span id="_defaultvalue__is_applied_to_a_non-VARIANT_and__optional_._Please_remove__optional_"></span><span id="_defaultvalue__is_applied_to_a_non-variant_and__optional_._please_remove__optional_"></span><span id="_DEFAULTVALUE__IS_APPLIED_TO_A_NON-VARIANT_AND__OPTIONAL_._PLEASE_REMOVE__OPTIONAL_"></span>[DefaultValue] wird auf eine nicht Variante und [optional] angewendet. Bitte entfernen [optional]</dt> <dd> Das Attribut [<a href="defaultvalue.md"><strong>DefaultValue</strong></a>] impliziert [<a href="optional.md"><strong>optional</strong></a>]. Das [ <strong>optional</strong>]-Attribut ist nicht erforderlich.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2402"></span><span id="midl2402"></span><dl> <dt><strong>MIDL2402</strong></dt> </dl></td>
<td><dl> <dt><span id="_optional__attribute_is_inapplicable_outside_of_a_library_block"></span><span id="_OPTIONAL__ATTRIBUTE_IS_INAPPLICABLE_OUTSIDE_OF_A_LIBRARY_BLOCK"></span>[optional] das Attribut ist außerhalb eines Bibliotheks Blocks nicht anwendbar.</dt> <dd> Die durch das [ <a href="optional.md"><strong>optional</strong></a>]-Attribut implizierten Funktionen können nicht auf Proxys angewendet werden, die für eine Schnittstelle außerhalb eines Bibliotheks Blocks generiert werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2403"></span><span id="midl2403"></span><dl> <dt><strong>MIDL2403</strong></dt> </dl></td>
<td><dl> <dt><span id="The_data_type_of_the__Icid__parameter_must_be_long"></span><span id="the_data_type_of_the__icid__parameter_must_be_long"></span><span id="THE_DATA_TYPE_OF_THE__ICID__PARAMETER_MUST_BE_LONG"></span>Der Datentyp des [ICID]-Parameters muss lang sein.</dt> <dd> Die OLE-Automatisierung erfordert, dass Parameter mit dem [<strong>ICID</strong>]-Attribut den Typ " <a href="long.md"><strong>Long</strong></a>" aufweisen müssen.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2404"></span><span id="midl2404"></span><dl> <dt><strong>MIDL2404</strong></dt> </dl></td>
<td><dl> <dt><span id="procedures_with__propput____propget__or__propref__can_t_have_more_than_one_required_parameter_after__optional__one"></span><span id="PROCEDURES_WITH__PROPPUT____PROPGET__OR__PROPREF__CAN_T_HAVE_MORE_THAN_ONE_REQUIRED_PARAMETER_AFTER__OPTIONAL__ONE"></span>Prozeduren mit [propput], [Propget] oder [propref] dürfen nicht mehr als einen erforderlichen Parameter nach [optional] aufweisen.</dt> <dd> Es darf nicht mehr als ein Parameter ohne [<a href="optional.md"><strong>optional</strong></a>] nach dem letzten Parameter mit [<strong>optional</strong>] vorhanden sein, wenn [<a href="propput.md"><strong>PROPPUT</strong></a>], [<a href="propget.md"><strong>propget</strong></a>] oder [ <a href="propputref.md"><strong>PROPPUTREF</strong></a>] verwendet wird.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2405"></span><span id="midl2405"></span><dl> <dt><strong>MIDL2405</strong></dt> </dl></td>
<td><dl> <dt><span id="_comm_status__or__fault_status__with_pickling_requires_-Oicf"></span><span id="_comm_status__or__fault_status__with_pickling_requires_-oicf"></span><span id="_COMM_STATUS__OR__FAULT_STATUS__WITH_PICKLING_REQUIRES_-OICF"></span>[comm_status] oder [fault_status] mit Pickup erfordert-Oicf</dt> <dd> Der Optimierungs Modus von alten<strong>Oi</strong> unterstützt keine Prozeduren oder Parameter mit [ <a href="comm-status.md"><strong>comm_status</strong></a>] oder [ <a href="fault-status.md"><strong>fault_status</strong></a>] mit Auswahl (d. h. mit [ <a href="encode.md"><strong>Codieren</strong></a>] und/oder [ <a href="decode.md"><strong>decodieren</strong></a>]).<br/> Diese Warnung kann Global unterdrückt werden, indem Sie-<strong>Oicf</strong> in der Mittell-Befehlszeile oder für eine einzelne Funktion angeben, indem &quot; Sie der Funktion in der ACF-Datei das Attribut [optimieren (ICF:)] hinzufügen.<br/> Im Allgemeinen wird der-<strong>Oicf</strong> -Optimierungs Modus im over-<strong>Oi</strong> -Modus empfohlen.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2406"></span><span id="midl2406"></span><dl> <dt><strong>MIDL2406</strong></dt> </dl></td>
<td><dl> <dt><span id="midl_driver_and_compiler_version_mismatch"></span><span id="MIDL_DRIVER_AND_COMPILER_VERSION_MISMATCH"></span>nicht übereinstimmende mittlere Treiber-und Compilerversionen</dt> <dd> Ab der Windows 2000-Version (mittlerer l-Version 5.03.279) wird der Mittelwert Compiler mithilfe von zwei ausführbaren Dateien implementiert: Midl.exe (Treiber) und Midlc.exe (die Compiler-Engine). Dieser Fehler weist darauf hin, dass die Version von Midl.exe nicht mit der Version von Midlc.exe identisch ist.<br/> Der Fehler ist möglicherweise darauf zurückzuführen, dass Midl.exe kopiert, jedoch nicht aus der letzten Verteilung Midlc.exe. Führen Sie in der Befehlszeile die Dateien " <strong>Mittel l</strong> " und/oder " <strong>mittellc</strong> " ohne Parameter aus, um die Versionsnummer der ausführbaren Datei anzuzeigen.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2407"></span><span id="midl2407"></span><dl> <dt><strong>MIDL2407</strong></dt> </dl></td>
<td><dl> <dt><span id="no_intermediate_file_specified__use_Midl.exe"></span><span id="no_intermediate_file_specified__use_midl.exe"></span><span id="NO_INTERMEDIATE_FILE_SPECIFIED__USE_MIDL.EXE"></span>Es wurde keine zwischen Datei angegeben: Verwenden Sie Midl.exe</dt> <dd> Ab der Windows 2000-Version (mittlerer l-Version 5.03.279) wird der Mittelwert Compiler mithilfe von zwei ausführbaren Dateien implementiert: Midl.exe (Treiber) und Midlc.exe (die Compiler-Engine). Dieser Fehler weist darauf hin, dass Midlc.exe direkt ausgeführt wurde, anstatt Midl.exe zu verwenden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2408"></span><span id="midl2408"></span><dl> <dt><strong>MIDL2408</strong></dt> </dl></td>
<td><dl> <dt><span id="processing_problem_with_a_parameter_in_a_procedure"></span><span id="PROCESSING_PROBLEM_WITH_A_PARAMETER_IN_A_PROCEDURE"></span>Verarbeiten eines Problems mit einem Parameter in einer Prozedur</dt> <dd> Dieser Fehler kann auftreten, wenn Daten aus einem tlb importiert werden und wenn eine Prozedur über einen ungültigen Parameter verfügt. <br/> Wenn dieser Fehler angezeigt wird, melden Sie einen Fehler an Microsoft. Geben Sie die IDL-Dateien, die ACF-Dateien, die TLB-Datei und die vollständige Mittell-Befehlszeile an.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2409"></span><span id="midl2409"></span><dl> <dt><strong>MIDL2409</strong></dt> </dl></td>
<td><dl> <dt><span id="processing_problem_with_a_field_in_a_structure"></span><span id="PROCESSING_PROBLEM_WITH_A_FIELD_IN_A_STRUCTURE"></span>Verarbeiten eines Problems mit einem Feld in einer Struktur</dt> <dd> Dieser Fehler kann auftreten, wenn Daten aus einem tlb importiert werden und wenn eine Struktur ein ungültiges Struktur-oder Union-Feld aufweist.<br/> Wenn dieser Fehler angezeigt wird, melden Sie einen Fehler an Microsoft. Geben Sie die IDL-Dateien, die ACF-Dateien, die TLB-Datei und die vollständige Mittell-Befehlszeile an.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2410"></span><span id="midl2410"></span><dl> <dt><strong>MIDL2410</strong></dt> </dl></td>
<td><dl> <dt><span id="internal_compiler_inconsistency_detected__the_format_string_offset_is_invalid._See_the_documentation_for_more_information."></span><span id="internal_compiler_inconsistency_detected__the_format_string_offset_is_invalid._see_the_documentation_for_more_information."></span><span id="INTERNAL_COMPILER_INCONSISTENCY_DETECTED__THE_FORMAT_STRING_OFFSET_IS_INVALID._SEE_THE_DOCUMENTATION_FOR_MORE_INFORMATION."></span>interne Compilerwarnung erkannt: der Offset der Format Zeichenfolge ist ungültig. Weitere Informationen finden Sie in der Dokumentation.</dt> <dd> Der mittlerer l-Compiler hat einen ungültigen Wert in seinen internen Datenstrukturen erkannt. Dies kann durch rekursive Strukturen oder durch Compiler verursacht werden, die seine eigenen Grenzwerte für die Darstellung interner Daten verletzen. Um das Problem zu identifizieren und/oder zu umgehen, versuchen Sie, die IDL-Datei zu vereinfachen. Hierzu können Sie komplexe Parameter und rekursive Datenstrukturen vereinfachen oder die IDL-Datei durch Aufteilen aufteilen. Diese Meldung wird möglicherweise von einem diagnoseprintout mit zusätzlichen Informationen über das Problem begleitet.<br/> Wenn dieser Fehler angezeigt wird, melden Sie einen Fehler an Microsoft. Geben Sie ggf. die IDL-Dateien, ACF-Dateien, die vollständige mittlere Befehlszeile und die Diagnoseausgabe an.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2411"></span><span id="midl2411"></span><dl> <dt><strong>MIDL2411</strong></dt> </dl></td>
<td><dl> <dt><span id="internal_compiler_inconsistency_detected__the_type_offset_is_invalid._See_the_documentation_for_more_information."></span><span id="internal_compiler_inconsistency_detected__the_type_offset_is_invalid._see_the_documentation_for_more_information."></span><span id="INTERNAL_COMPILER_INCONSISTENCY_DETECTED__THE_TYPE_OFFSET_IS_INVALID._SEE_THE_DOCUMENTATION_FOR_MORE_INFORMATION."></span>interne Compilerwarnung erkannt: der typoffset ist ungültig. Weitere Informationen finden Sie in der Dokumentation.</dt> <dd> Der mittlerer l-Compiler hat einen ungültigen Wert in seinen internen Datenstrukturen erkannt. Dies kann durch rekursive Strukturen oder durch den Compiler verursacht werden, die seine eigenen Grenzwerte für die Darstellung interner Daten verletzen. Um das Problem zu identifizieren und/oder zu umgehen, versuchen Sie, die IDL-Datei zu vereinfachen. Hierzu können Sie komplexe Parameter und rekursive Datenstrukturen vereinfachen oder die IDL-Datei durch Aufteilen aufteilen. Diese Meldung wird möglicherweise von einem diagnoseprintout mit zusätzlichen Informationen über das Problem begleitet.<br/> Wenn dieser Fehler angezeigt wird, melden Sie einen Fehler an Microsoft. Geben Sie ggf. die IDL-Dateien, ACF-Dateien, die vollständige mittlere Befehlszeile und die Diagnoseausgabe an.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2412"></span><span id="midl2412"></span><dl> <dt><strong>MIDL2412</strong></dt> </dl></td>
<td><dl> <dt><span id="SAFEARRAY_roo__syntax_is_not_supported_outside_of_the_library_block__use_LPSAFEARRAY_for_proxy"></span><span id="safearray_roo__syntax_is_not_supported_outside_of_the_library_block__use_lpsafearray_for_proxy"></span><span id="SAFEARRAY_ROO__SYNTAX_IS_NOT_SUPPORTED_OUTSIDE_OF_THE_LIBRARY_BLOCK__USE_LPSAFEARRAY_FOR_PROXY"></span>Die "SafeArray (Roo)"-Syntax wird außerhalb des Bibliotheks Blocks nicht unterstützt. verwenden Sie "lpsafearray" für den Proxy.</dt> <dd> Explizit typisierte SAFEARRAYs sind außerhalb eines Bibliotheks Blocks nicht zulässig. Verwenden Sie stattdessen lpsafearray.<br/> Dieser Fehler wird im folgenden Beispiel veranschaulicht:<br/>
<pre class="syntax" data-space="preserve"><code>void roo(SAFEARRAY(long) *a); //MIDL2412 when outside a library block
void roo(LPSAFEAEEAY a);         //OK</code></pre>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2413"></span><span id="midl2413"></span><dl> <dt><strong>MIDL2413</strong></dt> </dl></td>
<td><dl> <dt><span id="bit_fields_are_not_supported"></span><span id="BIT_FIELDS_ARE_NOT_SUPPORTED"></span>Bitfelder werden nicht unterstützt.</dt> <dd> Bitfelder im C-Stil werden von der Mittell nicht unterstützt. Dies gilt für die Generierung von Proxys und die TLB-Generierung.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2414"></span><span id="midl2414"></span><dl> <dt><strong>MIDL2414</strong></dt> </dl></td>
<td><dl> <dt><span id="floating_point_or_complex_return_types_with__decode__are_not_supported_in_-Oicf__using_-OI"></span><span id="floating_point_or_complex_return_types_with__decode__are_not_supported_in_-oicf__using_-oi"></span><span id="FLOATING_POINT_OR_COMPLEX_RETURN_TYPES_WITH__DECODE__ARE_NOT_SUPPORTED_IN_-OICF__USING_-OI"></span>Gleit Komma-oder komplexe Rückgabe Typen mit [Decode] werden in-Oicf nicht unterstützt. verwenden Sie-Oi.</dt> <dd> Prozeduren mit Gleit Komma-oder Struktur-/Union-Rückgabetypen werden in der-Oicf-Stil Auswahl nicht unterstützt. Eine Problem Umgehung für 32-Bit ist die Verwendung des-Oi-Optimierungs Modus beim Serialisieren von Daten (mit [Encode] und/oder [Decode]). Da der Unterstützung für den alten Oi-Interpreter und die Unterstützung für die Unterstützung nach der Veröffentlichung von Windows 2000 jedoch als veraltet festgelegt wird, wird die Verwendung von Zeigern dringend vorgeschlagen, wenn Sie dieses Problem umgehen. Beachten Sie auch, dass das Ändern einer Schnittstellen Methode zur Verwendung eines [out, REF]-Zeigers anstelle des Rückgabewerts, der das Problem verursacht, bei der Übertragung vollständig abwärts kompatibel ist und problemlos auf der APP-Ebene ausgeblendet werden kann. <br/> Diese Warnung kann Global unterdrückt werden, indem Sie-Oi in der Mittell-Befehlszeile oder für eine einzelne Funktion angeben, indem Sie das [optimieren ( &quot; i &quot; )]-Attribut zur Funktion in der ACF-Datei hinzufügen.<br/> Im folgenden Beispiel wird das Problem veranschaulicht:<br/> Roo. idl: <br/>
<pre class="syntax" data-space="preserve"><code>double GetDouble();</code></pre>
Roo. ACF: <br/>
<pre class="syntax" data-space="preserve"><code>[decode] GetDouble();</code></pre>
Eine Möglichkeit, diese Einschränkung zu umgehen, besteht darin, einen [out]-Parameter zu übergeben, um das Ergebnis zu speichern, anstatt einen Rückgabewert zu verwenden:<br/> Roo. idl: <br/>
<pre class="syntax" data-space="preserve"><code>void GetDouble([out] double *result); //top level pointer is a [ref] pointer</code></pre>
Roo. ACF: <br/>
<pre class="syntax" data-space="preserve"><code>[decode] GetDouble();</code></pre>
Wie bereits erwähnt, eignet sich die oben beschriebene Lösung nicht nur für die neuen Schnittstellen, sondern auch für die alten. Die Wire-Darstellung für das neue &quot; out- &quot; Argument ist identisch mit der für den Rückgabewert (Beachten Sie, dass der neue Rückgabewert void ist).<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2415"></span><span id="midl2415"></span><dl> <dt><strong>MIDL2415</strong></dt> </dl></td>
<td><dl> <dt><span id="the_return_type_is_not_supported_for_64-bit_when_using__decode_"></span><span id="THE_RETURN_TYPE_IS_NOT_SUPPORTED_FOR_64-BIT_WHEN_USING__DECODE_"></span>der Rückgabetyp wird bei Verwendung von [Decode] für 64-Bit nicht unterstützt.</dt> <dd> Prozeduren mit Gleit Komma-oder Struktur-/Union-Rückgabetypen werden beim Ausführen der Datenserialisierung (mit [ <a href="encode.md"><strong>Codieren</strong></a>] und/oder [ <a href="decode.md"><strong>decodieren</strong></a>]) im 64-Bit-Modus nicht unterstützt. Dies bezieht sich auf den alten Stil-Oi-Interpreter, und der datenserialisierer wird auf der 64-Bit-Plattform nicht unterstützt. Weitere Informationen finden Sie in der Beschreibung von MIDL2414. <br/> Dieser Fehler wird im folgenden Beispiel veranschaulicht:<br/> Roo. idl: <br/>
<pre class="syntax" data-space="preserve"><code>double GetDouble();</code></pre>
Roo. ACF: <br/>
<pre class="syntax" data-space="preserve"><code>[decode] GetDouble();</code></pre>
Folgendes wird als Problem Umgehung für neue und alte Schnittstellen empfohlen. Verwenden Sie einen [out]-Parameter, um das Ergebnis zu speichern, anstatt einen Rückgabewert zu verwenden:<br/> Roo. idl: <br/>
<pre class="syntax" data-space="preserve"><code>void GetDouble([out] double *result); //top level pointer is a [ref] pointer.</code></pre>
Roo. ACF: <br/>
<pre class="syntax" data-space="preserve"><code>[decode] GetDouble();</code></pre>
Beachten Sie, dass diese Lösung bei der Übertragung vollständig abwärts kompatibel ist, da die Wire-Darstellung eines [ref, out]-Zeigers oder eines Double-datumers mit dem eines Double-Wert identisch ist.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2416"></span><span id="midl2416"></span><dl> <dt><strong>MIDL2416</strong></dt> </dl></td>
<td><dl> <dt><span id="transmitted_type_may_not_contain_a_full_pointer_for_either__wire_marshal__or__user_marshal_"></span><span id="TRANSMITTED_TYPE_MAY_NOT_CONTAIN_A_FULL_POINTER_FOR_EITHER__WIRE_MARSHAL__OR__USER_MARSHAL_"></span>der übertragene Typ darf weder einen vollständigen Zeiger für [Wire_marshal] noch [user_marshal] enthalten.</dt> <dd> Typen mit [ <a href="wire-marshal.md"><strong>Wire_marshal</strong></a>]-oder [ <a href="user-marshal.md"><strong>user_marshal</strong></a>]-Attributen dürfen nicht vollständige ([ <strong>ptr</strong>]) Zeiger enthalten. Verwenden Sie stattdessen [ <a href="unique.md"><strong>Unique</strong></a>] oder [ <a href="ref.md"><strong>ref</strong></a>].<br/> Dieser Fehler wird im folgenden Beispiel veranschaulicht:<br/>
<pre class="syntax" data-space="preserve"><code>typedef struct
{
    [ptr] long *a;    //Should use [ref] or [unique] instead
}
st1;
typedef [wire_marshal(st1)] struct
{
    long a;
}
st2:
void roo(st2 *s);    //MIDL2416</code></pre>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2417"></span><span id="midl2417"></span><dl> <dt><strong>MIDL2417</strong></dt> </dl></td>
<td><dl> <dt><span id="transmitted_type_must_either_be_a_pointer_or_have_a_constant_size_for__wire_marshal__and__user_marshal_"></span><span id="TRANSMITTED_TYPE_MUST_EITHER_BE_A_POINTER_OR_HAVE_A_CONSTANT_SIZE_FOR__WIRE_MARSHAL__AND__USER_MARSHAL_"></span>der übertragene Typ muss entweder ein Zeiger sein oder eine konstante Größe für [Wire_marshal] und [user_marshal] aufweisen.</dt> <dd> Typen der obersten Ebene mit [ <a href="wire-marshal.md"><strong>Wire_marshal</strong></a>]-oder [ <a href="user-marshal.md"><strong>user_marshal</strong></a>]-Attributen müssen zur Kompilierzeit eine klar definierte Größe aufweisen. Sie dürfen keine Übereinstimmung oder Arrays mit unterschiedlichen Größen aufweisen oder enthalten.<br/> Dieser Fehler wird im folgenden Beispiel veranschaulicht:<br/>
<pre class="syntax" data-space="preserve"><code>typedef struct        //Type contains variable-sized array
{
    long s;
    [size_is(s)] char a[];
}
st1;
typedef [wire_marshal(st1)] struct
{
    long a;
}
st2;
void roo(st2 *s);        //MIDL2417</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2418"></span><span id="midl2418"></span><dl> <dt><strong>MIDL2418</strong></dt> </dl></td>
<td><dl> <dt><span id="procedures_with__propget__must_have_at_least_one_parameter_or_a_return_value"></span><span id="PROCEDURES_WITH__PROPGET__MUST_HAVE_AT_LEAST_ONE_PARAMETER_OR_A_RETURN_VALUE"></span>Prozeduren mit [Propget] müssen mindestens einen Parameter oder einen Rückgabewert aufweisen.</dt> <dd> Prozeduren mit dem [Propget]-Attribut müssen eine Möglichkeit haben, den Eigenschafts Wert zurückzugeben. Sie müssen mindestens einen [<a href="-out.md"><strong>out</strong></a>]-Parameter oder einen Rückgabewert aufweisen.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2461"></span><span id="midl2461"></span><dl> <dt><strong>MIDL2461</strong></dt> </dl></td>
<td><dl> <dt><span id="The__readonly__attribute_was_applied_at_the_method_level."></span><span id="the__readonly__attribute_was_applied_at_the_method_level."></span><span id="THE__READONLY__ATTRIBUTE_WAS_APPLIED_AT_THE_METHOD_LEVEL."></span>Das Attribut [schreibgeschützt] wurde auf Methoden Ebene angewendet.</dt> <dd> Das Attribut [schreibgeschützt] kann nur auf Parameter Ebene angewendet werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2465"></span><span id="midl2465"></span><dl> <dt><strong>MIDL2465</strong></dt> </dl></td>
<td><dl> <dt><span id="Structures_containing_conformant_arrays_must_be_passed_by_reference"></span><span id="structures_containing_conformant_arrays_must_be_passed_by_reference"></span><span id="STRUCTURES_CONTAINING_CONFORMANT_ARRAYS_MUST_BE_PASSED_BY_REFERENCE"></span>Strukturen, die konforme Arrays enthalten, müssen als Verweis bestanden werden.</dt> <dd> Parameter der obersten Ebene in RPC müssen zur Kompilierzeit eine klar definierte Größe aufweisen. Sie dürfen nicht sein oder ein Array mit Übereinstimmung oder variabler Breite enthalten. Außerdem können Benutzer einen Typ ohne klar definierte Größe nicht codieren/decodieren. Anwendungen müssen eine konforme Struktur/konforme Struktur durch Verweis übergeben.<br/> Dieser Fehler wird im folgenden Beispiel veranschaulicht:<br/>
<pre class="syntax" data-space="preserve"><code>typedef struct        //Type contains variable-sized array
{
    long s;
    [size_is(s)] char a[];
}
st1;
void roo(st1 s);        //MIDL2465
 
on .acf file
typedef [encode,decode] st1; //MIDL2465</code></pre>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL9008"></span><span id="midl9008"></span><dl> <dt><strong>MIDL9008</strong></dt> </dl></td>
<td><dl> <dt><span id="_internal_compiler_problem__system_error_code__-_the_compiler_cannot_continue_for_an_unknown_reason._See_documentation_for_a_workaround."></span><span id="_internal_compiler_problem__system_error_code__-_the_compiler_cannot_continue_for_an_unknown_reason._see_documentation_for_a_workaround."></span><span id="_INTERNAL_COMPILER_PROBLEM__SYSTEM_ERROR_CODE__-_THE_COMPILER_CANNOT_CONTINUE_FOR_AN_UNKNOWN_REASON._SEE_DOCUMENTATION_FOR_A_WORKAROUND."></span> interner Compilerfehler <system error code> - : der Compiler kann aus unbekannten Gründen nicht fortgesetzt werden. Eine Problem Umgehung finden Sie in der Dokumentation.</dt> <dd> Der Compiler konnte nicht fortgesetzt werden, und die Ursache des Fehlers ist unbekannt. Die hexadezimale Fehlernummer ist ein Systemfehler Bezeichner. Bei der Kompilierung ist möglicherweise ein Fehler aufgrund eines externen Problems aufgetreten, z. b. aufgrund von nicht genügend Arbeitsspeicher. In diesem Fall finden Sie weitere Informationen in "Winerror. h" oder "NTSTATUS. h". <br/> Es gibt zwei Situationen, in denen dieser Fehler normalerweise generiert wird:<br/>
<ul>
<li>Der mittlerer l-Compiler konnte nach dem Erkennen eines Fehlers in der IDL-Datei nicht wieder hergestellt werden. Wenn die Mittel l Fehlermeldungen zu ihrer IDL-Datei zurückgibt, versuchen Sie, Sie zu beheben und neu zu kompilieren. Wenn keine Fehlermeldungen vorliegen, ist der Compiler möglicherweise fehlgeschlagen, bevor ein Fehler gemeldet werden konnte. Suchen Sie in der Zeile, für die der interne Compilerfehler gemeldet wird, nach einem Syntax Fehler.</li>
<li>Der mittlerer l-Compiler konnte keinen korrekten Code unter einer angegebenen Optimierungs Option generieren. Versuchen Sie, compilermodi zu ändern, im gemischten Modus zu kompilieren (/<a href="-os.md"><strong>OS</strong></a>) oder alle Optimierungen zu entfernen. Sie können auch mit dem/NO_FORMAT_OPT-Flag erneut kompilieren, um die Standard Optimierung von Prozeduren und Typdeskriptoren in der Mitte zu unterdrücken.</li>
</ul>
Dieser Fehler tritt gelegentlich auf, auch wenn die IDL-Datei richtig ist und keine Optimierungs Optionen verwendet werden. Wenn dies der Fall ist, versuchen Sie, den Code Abschnitt in der Nähe der Fehlermeldung neu zu schreiben, indem Sie alle aktuellen Änderungen entfernen, Datentypen vereinfachen oder neu anordnen, Prototypen ändern oder andere Teile der IDL-Datei auskommentieren, um den Problemcode zu finden.<br/> Wenn keine dieser Optionen funktioniert, oder wenn Sie der Ansicht sind, dass das Problem möglicherweise auf einen Fehler in Midl.exe bezogen ist, Benachrichtigen Sie Microsoft, und geben Sie alle relevanten Details an.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



 

