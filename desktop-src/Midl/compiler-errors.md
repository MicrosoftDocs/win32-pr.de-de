---
title: Compilerfehler
description: Liste der Fehlermeldungen, die während der MIDL-Kompilierung generiert wurden.
ms.assetid: 492eacdd-6bd1-49df-9112-3765f6c05f34
keywords:
- Fehler MIDL, Compilerfehler
topic_type:
- apiref
api_name:
- Compiler Errors
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 04bfb8f3465849215711ff70b9d9d67e40817f4e
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884605"
---
# <a name="compiler-errors"></a>Compilerfehler

Die folgenden Fehlermeldungen werden während der MIDL-Kompilierung generiert:



<table>
<colgroup>
<col  />
<col  />
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
<td><dl> <dt><span id="must_specify__c_ext_for_abstract_declarators"></span><span id="MUST_SPECIFY__C_EXT_FOR_ABSTRACT_DECLARATORS"></span>muss /c_ext für abstrakte Deklaratoren angeben.</dt> <dd> Abstrakte Deklaratoren stellen eine Microsoft-Erweiterung für RPC dar und sind nicht in DCE RPC definiert. Wenn Ihre Datei abstrakte Deklaratoren enthält, können Sie daher nicht mit dem <a href="-osf.md"><strong>Schalter /osf</strong></a> kompilieren, wodurch eine strenge DCE-Kompatibilität erzwungen wird. MIDL-Versionen 3.0 und höher verwenden den <a href="-c-ext.md"><strong>Schalter /c_ext</strong></a> als Standard; Der <strong>Schalter /osf</strong> schaltet den <strong>Schalter /c_ext</strong> aus. Informationen zu abstrakten Deklaratoren finden Sie unter <a href="/windows/desktop/Rpc/the-acf-body">The ACF Body</a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2001"></span><span id="midl2001"></span><dl> <dt><strong>MIDL2001</strong></dt> </dl></td>
<td><dl> <dt><span id="instantiation_of_data_is_illegal__you_must_use__extern__or__static_"></span><span id="INSTANTIATION_OF_DATA_IS_ILLEGAL__YOU_MUST_USE__EXTERN__OR__STATIC_"></span>Die Instanziierung von Daten ist unzulässig. Sie müssen extern &quot; oder &quot; static &quot; verwenden.&quot;</dt> <dd> Deklaration und Initialisierung in der IDL-Datei sind nicht mit DCE RPC kompatibel. Dieses Feature ist eine Microsoft-Erweiterung, die bei der Kompilierung im DCE-Kompatibilitätsmodus<a href="-osf.md"><strong>(/osf)</strong></a>nicht verfügbar ist.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2002"></span><span id="midl2002"></span><dl> <dt><strong>MIDL2002</strong></dt> </dl></td>
<td><dl> <dt><span id="compiler_stack_overflow"></span><span id="COMPILER_STACK_OVERFLOW"></span>Compilerstapelüberlauf</dt> <dd> Beim Verarbeiten der IDL-Datei ist dem Compiler nicht mehr der Stapelspeicherplatz zur Verfügung. Dieses Problem kann auftreten, wenn der Compiler eine komplexe Deklaration oder einen komplexen Ausdruck verarbeitet. Vereinfachen Sie die komplexe Deklaration oder den komplexen Ausdruck, um das Problem zu lösen.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2003"></span><span id="midl2003"></span><dl> <dt><strong>MIDL2003</strong></dt> </dl></td>
<td><dl> <dt><span id="redefinition"></span><span id="REDEFINITION"></span>Neudefinition</dt> <dd> Diese Fehlermeldung kann unter den folgenden Umständen angezeigt werden: Ein Typ wurde neu definiert. ein Prozedurprototyp wurde neu definiert. ein Member einer Struktur oder Union mit dem gleichen Namen ist bereits vorhanden. Ein Parameter mit demselben Namen ist bereits im Prototyp vorhanden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2004"></span><span id="midl2004"></span><dl> <dt><strong>MIDL2004</strong></dt> </dl></td>
<td><dl> <dt><span id="_auto_handle__binding_will_be_used"></span><span id="_AUTO_HANDLE__BINDING_WILL_BE_USED"></span>[auto_handle] Bindung wird verwendet.</dt> <dd> Es wurde kein Handletyp als Standardhandpunkttyp definiert. Der Compiler geht davon aus, dass ein automatisches Handle als Bindungshand handle für die angegebene Prozedur verwendet wird.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2005"></span><span id="midl2005"></span><dl> <dt><strong>MIDL2005</strong></dt> </dl></td>
<td><dl> <dt><span id="out_of_memory"></span><span id="OUT_OF_MEMORY"></span>Nicht genügend Arbeitsspeicher</dt> <dd> Der Compiler hat während der Kompilierung nicht genügend Arbeitsspeicher. Verringern Sie die Größe oder Komplexität der IDL-Datei, oder weisen Sie dem Prozess mehr Arbeitsspeicher zu.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2006"></span><span id="midl2006"></span><dl> <dt><strong>MIDL2006</strong></dt> </dl></td>
<td><dl> <dt><span id="recursive_definition"></span><span id="RECURSIVE_DEFINITION"></span>rekursive Definition</dt> <dd> Eine Struktur oder Union wurde rekursiv definiert. Dieser Fehler kann auftreten, wenn eine Zeigerspezifikation in einer Definition einer geschachtelten Struktur übersehen wird.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2007"></span><span id="midl2007"></span><dl> <dt><strong>MIDL2007</strong></dt> </dl></td>
<td><dl> <dt><span id="import_ignored__file_already_imported"></span><span id="IMPORT_IGNORED__FILE_ALREADY_IMPORTED"></span>Import ignoriert; Bereits importierte Datei</dt> <dd> Das Importieren einer IDL-Datei ist ein idempotenter Vorgang. Das Mehr-als-einmal-Einlesen hat keine Auswirkungen. Alle außer dem ersten Importvorgang werden ignoriert.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2008"></span><span id="midl2008"></span><dl> <dt><strong>MIDL2008</strong></dt> </dl></td>
<td><dl> <dt><span id="sparse_enums_require__c_ext_or__ms_ext"></span><span id="SPARSE_ENUMS_REQUIRE__C_EXT_OR__MS_EXT"></span>Sparseenumen erfordern /c_ext oder /ms_ext</dt> <dd> Das Zuweisen von Werten zu Enumerationskonst constants ist nicht mit DCE RPC kompatibel. Wenn Sie die Microsoft-Erweiterungen für MIDL verwenden möchten, die das Zuweisen von Werten zu Enumerationskonst constants ermöglichen, können Sie nicht mit dem <a href="-osf.md"><strong>Schalter /osf</strong></a> kompilieren, wodurch eine strenge DCE-Kompatibilität erzwungen wird. MIDL-Versionen 3.0 und höher verwenden die Schalter <a href="-c-ext.md"><strong>/c_ext</strong></a> und <a href="-ms-ext.md"><strong>/ms_ext</strong></a> als Standard; Der <strong>Schalter /osf</strong> deaktiviert diese Erweiterungsschalter.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2009"></span><span id="midl2009"></span><dl> <dt><strong>MIDL2009</strong></dt> </dl></td>
<td><dl> <dt><span id="undefined_symbol"></span><span id="UNDEFINED_SYMBOL"></span>Nicht definiertes Symbol</dt> <dd> Ein nicht definiertes Symbol wurde in einem Ausdruck verwendet. Dieser Fehler kann auftreten, wenn Sie einen nicht definierten enumerierten Wert verwenden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2010"></span><span id="midl2010"></span><dl> <dt><strong>MIDL2010</strong></dt> </dl></td>
<td><dl> <dt><span id="type_used_in_ACF_file_not_defined_in_IDL_file"></span><span id="type_used_in_acf_file_not_defined_in_idl_file"></span><span id="TYPE_USED_IN_ACF_FILE_NOT_DEFINED_IN_IDL_FILE"></span>Typ, der in einer ACF-Datei verwendet wird, die nicht in der IDL-Datei definiert ist</dt> <dd> Ein nicht definierter Typ wird verwendet.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2011"></span><span id="midl2011"></span><dl> <dt><strong>MIDL2011</strong></dt> </dl></td>
<td><dl> <dt><span id="unresolved_type_declaration"></span><span id="UNRESOLVED_TYPE_DECLARATION"></span>Nicht aufgelöste Typdeklaration</dt> <dd> Der im Feld "Zusätzliche Fehlerinformationen" gemeldete Typ wurde an anderer Stelle in der IDL-Datei nicht definiert.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2012"></span><span id="midl2012"></span><dl> <dt><strong>MIDL2012</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_wide-character_constants_requires__ms_ext_or__c_ext"></span><span id="USE_OF_WIDE-CHARACTER_CONSTANTS_REQUIRES__MS_EXT_OR__C_EXT"></span>Die Verwendung von Breitzeichenkonst konstanten erfordert /ms_ext oder /c_ext</dt> <dd> Breitzeichenkonst constants sind eine Microsoft-Erweiterung für DCE IDL. Um den Datentyp <a href="wchar-t.md"><strong>wchar_t</strong></a>zu verwenden, können Sie nicht mit dem <a href="-osf.md"><strong>Schalter /osf</strong></a> kompilieren, der die MIDL-Compiler-Standardschalter <a href="-ms-ext.md"><strong>/ms_ext</strong></a> und <a href="-c-ext.md"><strong>/c_ext.</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2013"></span><span id="midl2013"></span><dl> <dt><strong>MIDL2013</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_wide_character_strings_requires__ms_ext_or__c_ext"></span><span id="USE_OF_WIDE_CHARACTER_STRINGS_REQUIRES__MS_EXT_OR__C_EXT"></span>Die Verwendung von Breitzeichenzeichenfolgen erfordert /ms_ext oder /c_ext</dt> <dd> Zeichenfolgenkonst constants mit Breitzeichen sind eine Microsoft-Erweiterung für DCE-IDL. Um den Datentyp <a href="wchar-t.md"><strong>wchar_t</strong></a>zu verwenden, können Sie nicht mit dem <a href="-osf.md"><strong>Schalter /osf</strong></a> kompilieren, der die MIDL-Compiler-Standardschalter <a href="-ms-ext.md"><strong>/ms_ext</strong></a> und <a href="-c-ext.md"><strong>/c_ext.</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2014"></span><span id="midl2014"></span><dl> <dt><strong>MIDL2014</strong></dt> </dl></td>
<td><dl> <dt><span id="inconsistent_redefinition_of_type_wchar_t"></span><span id="INCONSISTENT_REDEFINITION_OF_TYPE_WCHAR_T"></span>Inkonsistente Neudefinition des Typs wchar_t</dt> <dd> Der Typ <a href="wchar-t.md"><strong>wchar_t</strong></a> wurde als Typ neu definiert, der nicht gleichbedeutend mit unsigned short DOS * ist.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2015"></span><span id="midl2015"></span><dl> <dt><strong>MIDL2015</strong></dt> </dl></td>
<td><dl> <dt><span id="importlib_not_found"></span><span id="IMPORTLIB_NOT_FOUND"></span>importlib nicht gefunden</dt> <dd> Der Compiler konnte die durch die <a href="importlib.md"><strong>[importlib</strong></a>]-Direktive angegebene Typbibliothek nicht finden. Überprüfen Sie, ob der Pfad und der Name der Bibliothek richtig sind.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2016"></span><span id="midl2016"></span><dl> <dt><strong>MIDL2016</strong></dt> </dl></td>
<td><dl> <dt><span id="two_library_blocks"></span><span id="TWO_LIBRARY_BLOCKS"></span>Zwei Bibliotheksblöcke</dt> <dd> Zwei Bibliotheksblöcke (auch mit unterschiedlichen Namen) in derselben Quelldatei sind ungültig. Kombinieren Sie alle Elemente in einem einzigen Bibliotheksblock.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2017"></span><span id="midl2017"></span><dl> <dt><strong>MIDL2017</strong></dt> </dl></td>
<td><dl> <dt><span id="the_dispinterface_statement_requires_a_definition_for_IDispatch"></span><span id="the_dispinterface_statement_requires_a_definition_for_idispatch"></span><span id="THE_DISPINTERFACE_STATEMENT_REQUIRES_A_DEFINITION_FOR_IDISPATCH"></span>Die dispinterface-Anweisung erfordert eine Definition für IDispatch.</dt> <dd> Dieser Fehler tritt im Allgemeinen auf, wenn die Dateien Stdole2.tlb oder Oaidl.idl nicht importiert werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2018"></span><span id="midl2018"></span><dl> <dt><strong>MIDL2018</strong></dt> </dl></td>
<td><dl> <dt><span id="error_accessing_type_library"></span><span id="ERROR_ACCESSING_TYPE_LIBRARY"></span>Fehler beim Zugreifen auf die Typbibliothek</dt> <dd> Der Compiler konnte die angegebene Typbibliothek nicht finden. Stellen Sie sicher, dass Sie den Pfad richtig angegeben haben.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2019"></span><span id="midl2019"></span><dl> <dt><strong>MIDL2019</strong></dt> </dl></td>
<td><dl> <dt><span id="error_accessing_type_info"></span><span id="ERROR_ACCESSING_TYPE_INFO"></span>Fehler beim Zugreifen auf Typinformationen</dt> <dd> Die importierte Typbibliothek ist beschädigt, ungültig oder nur teilweise konstruiert.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2020"></span><span id="midl2020"></span><dl> <dt><strong>MIDL2020</strong></dt> </dl></td>
<td><dl> <dt><span id="error_generating_type_library"></span><span id="ERROR_GENERATING_TYPE_LIBRARY"></span>Fehler beim Generieren der Typbibliothek</dt> <dd> Die Typbibliothek konnte nicht generiert werden. Eine mögliche Ursache für diesen Fehler ist das Angeben eines Pfads zur IDL-Datei, der länger als 126 Zeichen ist. Oleaut32.dll unterstützt keine Pfadnamen, die länger als 126 Zeichen sind.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2021"></span><span id="midl2021"></span><dl> <dt><strong>MIDL2021</strong></dt> </dl></td>
<td><dl> <dt><span id="duplicate_id"></span><span id="DUPLICATE_ID"></span>Doppelte ID</dt> <dd> Anwendungen verwenden die <a href="id.md"><strong>ID-Anweisung</strong></a> in IDL-Dateien, um eine DISPID für Memberfunktionen anzugeben. Die Memberfunktionen können Eigenschaften oder Methoden von Schnittstellen oder Disp-Schnittstellen sein. Dieser Fehler gibt an, dass die IDL-Datei die gleiche Bezeichnernummer für zwei Methoden oder Eigenschaften angibt.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2022"></span><span id="midl2022"></span><dl> <dt><strong>MIDL2022</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_or_missing_value_for_entry_attribute"></span><span id="ILLEGAL_OR_MISSING_VALUE_FOR_ENTRY_ATTRIBUTE"></span>Ungültiger oder fehlender Wert für das Eintragsattribut</dt> <dd> Das Argument für das Entry-Attribut kann entweder eine Zeichenfolge sein, die einen benannten Einstiegspunkt angibt, oder eine Ordnungszahl, die den Einstiegspunkt definiert. Dieses Argument fehlt oder enthält einen ungültigen Wert.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2023"></span><span id="midl2023"></span><dl> <dt><strong>MIDL2023</strong></dt> </dl></td>
<td><dl> <dt><span id="error_recovery_assumes"></span><span id="ERROR_RECOVERY_ASSUMES"></span>Bei der Fehlerwiederherstellung wird davon ausgegangen.</dt> <dd> Der MIDL-Compiler hat ungültige Zeichen in der IDL-Datei gefunden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2024"></span><span id="midl2024"></span><dl> <dt><strong>MIDL2024</strong></dt> </dl></td>
<td><dl> <dt><span id="error_recovery_discards"></span><span id="ERROR_RECOVERY_DISCARDS"></span>Fehlerwiederherstellung verwirft</dt> <dd> Der MIDL-Compiler hat ungültige Zeichen in der IDL-Datei gefunden. Die ungültigen Zeichen werden ignoriert.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2025"></span><span id="midl2025"></span><dl> <dt><strong>MIDL2025</strong></dt> </dl></td>
<td><dl> <dt><span id="syntax_error"></span><span id="SYNTAX_ERROR"></span>Syntaxfehler</dt> <dd> Der Compiler hat einen Syntaxfehler in der angegebenen Zeile erkannt.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2026"></span><span id="midl2026"></span><dl> <dt><strong>MIDL2026</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_recover_from_earlier_syntax_errors__aborting_compilation"></span><span id="CANNOT_RECOVER_FROM_EARLIER_SYNTAX_ERRORS__ABORTING_COMPILATION"></span>kann nach früheren Syntaxfehlern nicht wiederhergestellt werden. Abbruch der Kompilierung</dt> <dd> Der MIDL-Compiler versucht automatisch, nach Syntaxfehlern wiederherzustellen, indem syntaktische Elemente hinzugefügt oder entfernt werden. Diese Meldung weist darauf hin, dass der Compiler trotz dieser Wiederherstellungsversuche zu viele Fehler erkannt hat. Korrigieren Sie die angegebenen Fehler, und kompilieren Sie sie erneut.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2027"></span><span id="midl2027"></span><dl> <dt><strong>MIDL2027</strong></dt> </dl></td>
<td><dl> <dt><span id="unknown_pragma_option"></span><span id="UNKNOWN_PRAGMA_OPTION"></span>Unbekannte Pragmaoption</dt> <dd> Das angegebene C-Pragma wird in MIDL nicht unterstützt. Entfernen Sie das Pragma aus der IDL-Datei.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2028"></span><span id="midl2028"></span><dl> <dt><strong>MIDL2028</strong></dt> </dl></td>
<td><dl> <dt><span id="feature_not_implemented"></span><span id="FEATURE_NOT_IMPLEMENTED"></span>Nicht implementiertes Feature</dt> <dd> Das MIDL-Feature ist zwar Teil der Sprachdefinition, wird jedoch nicht in Microsoft RPC implementiert und wird vom MIDL-Compiler nicht unterstützt. Beispielsweise werden die folgenden Sprachfeatures nicht implementiert: bitset, pipe und der internationale Zeichentyp. Die Nichtimplementierte Sprachfunktion wird im zusätzlichen Fehlerinformationsfeld der Fehlermeldung angezeigt.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2029"></span><span id="midl2029"></span><dl> <dt><strong>MIDL2029</strong></dt> </dl></td>
<td><dl> <dt><span id="type_not_implemented"></span><span id="TYPE_NOT_IMPLEMENTED"></span>Typ nicht implementiert</dt> <dd> Der angegebene Datentyp ist zwar ein legales MIDL-Schlüsselwort, aber nicht in Microsoft RPC implementiert.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2030"></span><span id="midl2030"></span><dl> <dt><strong>MIDL2030</strong></dt> </dl></td>
<td><dl> <dt><span id="non-pointer_used_in_a_dereference_operation"></span><span id="NON-POINTER_USED_IN_A_DEREFERENCE_OPERATION"></span>Nichtzeiger, der in einem Dereferenzieren verwendet wird</dt> <dd> Ein Datentyp, der kein Zeiger ist, wurde Zeigervorgängen zugeordnet. Sie können nicht über den angegebenen Nichtzeiger auf das Objekt zugreifen.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2031"></span><span id="midl2031"></span><dl> <dt><strong>MIDL2031</strong></dt> </dl></td>
<td><dl> <dt><span id="expression_has_a_divide_by_zero"></span><span id="EXPRESSION_HAS_A_DIVIDE_BY_ZERO"></span>expression weist eine Division durch 0 (null) auf.</dt> <dd> Der konstante Ausdruck enthält division durch 0 (null).<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2032"></span><span id="midl2032"></span><dl> <dt><strong>MIDL2032</strong></dt> </dl></td>
<td><dl> <dt><span id="expression_uses_incompatible_types"></span><span id="EXPRESSION_USES_INCOMPATIBLE_TYPES"></span>expression verwendet inkompatible Typen.</dt> <dd> Die linke und rechte Seite des Operators in einem Ausdruck sind von inkompatiblen Typen.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2033"></span><span id="midl2033"></span><dl> <dt><strong>MIDL2033</strong></dt> </dl></td>
<td><dl> <dt><span id="nonarray_expression_uses_index_operator"></span><span id="NONARRAY_EXPRESSION_USES_INDEX_OPERATOR"></span>Nichtarrayausdruck verwendet Indexoperator</dt> <dd> Der Ausdruck verwendet den Arrayindizierungsvorgang für ein Datenelement, das nicht vom Arraytyp ist.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2034"></span><span id="midl2034"></span><dl> <dt><strong>MIDL2034</strong></dt> </dl></td>
<td><dl> <dt><span id="left-hand_side_of_expression_does_not_evaluate_to_struct_union_enum"></span><span id="LEFT-HAND_SIDE_OF_EXPRESSION_DOES_NOT_EVALUATE_TO_STRUCT_UNION_ENUM"></span>Die linke Seite des Ausdrucks wird nicht als Struktur/Union/Enumeration ausgewertet.</dt> <dd> Der direkte oder indirekte Verweisoperator &quot; oder wurde auf ein &quot; &quot; -> &quot; Datenobjekt angewendet, das keine Struktur, Union oder Enumeration ist. Sie können keinen direkten oder indirekten Verweis mit dem angegebenen -Objekt abrufen.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2035"></span><span id="midl2035"></span><dl> <dt><strong>MIDL2035</strong></dt> </dl></td>
<td><dl> <dt><span id="constant_expression_expected"></span><span id="CONSTANT_EXPRESSION_EXPECTED"></span>Konstanter Ausdruck erwartet</dt> <dd> Ein konstanter Ausdruck wurde in der Syntax erwartet. Arraygrenzen erfordern beispielsweise einen konstanten Ausdruck. Der Compiler gibt diese Fehlermeldung aus, wenn die Arraygrenze mit einer Variablen oder einem nicht definierten Symbol definiert wird.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2036"></span><span id="midl2036"></span><dl> <dt><strong>MIDL2036</strong></dt> </dl></td>
<td><dl> <dt><span id="expression_cannot_be_evaluated_at_compile_time"></span><span id="EXPRESSION_CANNOT_BE_EVALUATED_AT_COMPILE_TIME"></span>Expression kann zur Kompilierzeit nicht ausgewertet werden</dt> <dd> Der Compiler kann einen Ausdruck zur Kompilierzeit nicht auswerten.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2037"></span><span id="midl2037"></span><dl> <dt><strong>MIDL2037</strong></dt> </dl></td>
<td><dl> <dt><span id="expression_not_implemented"></span><span id="EXPRESSION_NOT_IMPLEMENTED"></span>Ausdruck nicht implementiert</dt> <dd> Ein Feature, das in früheren Versionen des MIDL-Compilers unterstützt wurde, wird in der Version des Compilers, der mit Microsoft RPC bereitgestellt wurde, nicht unterstützt. Entfernen Sie den angegebenen Ausdruck.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2038"></span><span id="midl2038"></span><dl> <dt><strong>MIDL2038</strong></dt> </dl></td>
<td><dl> <dt><span id="no__pointer_default__attribute_specified__assuming__unique__for_all_unattributed_pointers"></span><span id="NO__POINTER_DEFAULT__ATTRIBUTE_SPECIFIED__ASSUMING__UNIQUE__FOR_ALL_UNATTRIBUTED_POINTERS"></span>kein [pointer_default]-Attribut angegeben, vorausgesetzt[ unique] für alle nicht attributierten Zeiger</dt> <dd> Der MIDL-Compiler bietet drei verschiedene Standardfälle für Zeiger ohne Zeigerattribute. Funktionsparameter, bei denen es sich um Zeiger der obersten Ebene handelt, werden standardmäßig auf<a href="ref.md"><strong>[ref]-Zeiger</strong></a>verwendet. Zeiger, die in Strukturen eingebettet sind, und Zeiger auf andere Zeiger (keine Zeiger der obersten Ebene) werden standardmäßig auf den Typ festgelegt, der vom Attribut [<a href="pointer-default.md"><strong>pointer_default</strong></a>] angegeben wird. Wenn kein [<strong>pointer_default</strong>] -Attribut angegeben wird, werden diese Zeiger auf nicht auf der Ebene der Ebene enthaltene Zeiger standardmäßig auf eindeutige Zeiger zurückgestellt. Diese Fehlermeldung gibt den letzten Fall an: Es wird kein Attribut [<strong>pointer_default</strong>] angegeben, und es gibt mindestens einen Zeiger der obersten Ebene, der als eindeutiger Zeiger behandelt wird. Weitere Informationen finden Sie unter <a href="/windows/desktop/Rpc/default-pointer-types">Standardzeigertypen.</a><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2039"></span><span id="midl2039"></span><dl> <dt><strong>MIDL2039</strong></dt> </dl></td>
<td><dl> <dt><span id="interface_is_not_automation_marshaling_conformant"></span><span id="INTERFACE_IS_NOT_AUTOMATION_MARSHALING_CONFORMANT"></span>Interface is not automation marshaling conformant (Schnittstelle ist kein automatisierungskonformes Marshalling)</dt> <dd> Die -Schnittstelle erfüllt nicht die Anforderungen für eine OLE-Automatisierungsschnittstelle. Überprüfen Sie, ob die Schnittstelle von <strong>IUnknown</strong> oder <strong>IDispatch</strong>abgeleitet ist.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2040"></span><span id="midl2040"></span><dl> <dt><strong>MIDL2040</strong></dt> </dl></td>
<td><dl> <dt><span id="_out__only_parameter_cannot_be_a_pointer_to_an_open_structure"></span><span id="_OUT__ONLY_PARAMETER_CANNOT_BE_A_POINTER_TO_AN_OPEN_STRUCTURE"></span>[out] Nur der Parameter kann kein Zeiger auf eine offene Struktur sein.</dt> <dd> Ein<a href="out-idl.md"><strong></strong></a>[out]-only-Parameter wurde als Zeiger auf eine Struktur verwendet, die als offene Struktur bezeichnet wird, deren übertragener Bereich und größe zur Laufzeit bestimmt werden. Der Serverstub weiß nicht, wie viel Speicherplatz für eine offene Struktur belegt werden soll. Verwenden Sie einen Zeiger auf einen Zeiger auf die geöffnete Struktur, und stellen Sie sicher, dass die Serveranwendung ausreichend Speicherplatz dafür zuweist.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2041"></span><span id="midl2041"></span><dl> <dt><strong>MIDL2041</strong></dt> </dl></td>
<td><dl> <dt><span id="_out__only_parameter_cannot_be_an_unsized_string"></span><span id="_OUT__ONLY_PARAMETER_CANNOT_BE_AN_UNSIZED_STRING"></span>[out] Nur der Parameter darf keine nicht standardisierte Zeichenfolge sein.</dt> <dd> Ein Array mit dem Zeichenfolgenattribut wurde als [out]-only-Parameter ohne Größenangabe deklariert.<a href="out-idl.md"><strong></strong></a> Der Serverstub benötigt Größeninformationen, um Speicher für die Zeichenfolge zuzuordnen. Sie können das Zeichenfolgenattribut entfernen und das Attribut [<a href="size-is.md"><strong>size_is</strong></a>] hinzufügen, oder Sie können den Parameter in einen<strong>[in,out]-Parameter</strong>ändern.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2042"></span><span id="midl2042"></span><dl> <dt><strong>MIDL2042</strong></dt> </dl></td>
<td><dl> <dt><span id="_out__parameter_is_not_a_pointer"></span><span id="_OUT__PARAMETER_IS_NOT_A_POINTER"></span>[out]-Parameter ist kein Zeiger</dt> <dd> Alle<a href="out-idl.md"><strong>[out]-Parameter</strong></a>müssen Zeiger sein, die der Aufruf-nach-Wert-Konvention der Programmiersprache C entsprechen. Der<strong></strong>[out]-Richtungsparameter gibt an, dass der Server einen Wert an den Client überträgt. Mit der Aufruf-nach-Wert-Konvention kann der Server Daten nur dann an den Client übertragen, wenn das Funktionsargument ein Zeiger ist.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2043"></span><span id="midl2043"></span><dl> <dt><strong>MIDL2043</strong></dt> </dl></td>
<td><dl> <dt><span id="open_structure_cannot_be_a_parameter"></span><span id="OPEN_STRUCTURE_CANNOT_BE_A_PARAMETER"></span>Open-Struktur kann kein Parameter sein</dt> <dd> Eine offene -Struktur enthält ein konformes Array als letztes Element. Eine Struktur oder Union wird abgeschnitten, wenn das letzte Element dieser Struktur oder Union ein konformes Array ist.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2044"></span><span id="midl2044"></span><dl> <dt><strong>MIDL2044</strong></dt> </dl></td>
<td><dl> <dt><span id="_out__context_handle_generic_handle_must_be_specified_as_a_pointer_to_that_handle_type"></span><span id="_OUT__CONTEXT_HANDLE_GENERIC_HANDLE_MUST_BE_SPECIFIED_AS_A_POINTER_TO_THAT_HANDLE_TYPE"></span>[out] Kontexthandle/generisches Handle muss als Zeiger auf diesen Handletyp angegeben werden.</dt> <dd> Ein kontextbezogenes Handle oder ein benutzerdefinierter Handleparameter mit dem direktionalen Attribut [<a href="out-idl.md"><strong>out</strong></a>] muss ein Zeiger auf einen Zeiger sein.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2045"></span><span id="midl2045"></span><dl> <dt><strong>MIDL2045</strong></dt> </dl></td>
<td><dl> <dt><span id="context_handle_must_not_derive_from_a_type_that_has_the__transmit_as__attribute"></span><span id="CONTEXT_HANDLE_MUST_NOT_DERIVE_FROM_A_TYPE_THAT_HAS_THE__TRANSMIT_AS__ATTRIBUTE"></span>Das Kontexthandle darf nicht von einem Typ abgeleitet werden, der über das Attribut [transmit_as] verfügt.</dt> <dd> Kontexthandles müssen als Kontexthandletypen übertragen werden. Sie können nicht als andere Typen übertragen werden und können nicht von [transmit_is], [<strong>represent_as</strong>], [<strong>wire_marshal</strong>] oder [<strong>user_marshal</strong>] abgeleitet werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2046"></span><span id="midl2046"></span><dl> <dt><strong>MIDL2046</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_specify_a_variable_number_of_arguments_to_a_remote_procedure"></span><span id="CANNOT_SPECIFY_A_VARIABLE_NUMBER_OF_ARGUMENTS_TO_A_REMOTE_PROCEDURE"></span>kann keine variable Anzahl von Argumenten für eine Remoteprozedur angeben.</dt> <dd> Remoteprozeduraufrufe, die eine variable Anzahl von Argumenten zur Kompilierzeit angeben, sind nicht mit der DCE-RPC-Definition kompatibel. Sie können keine variable Anzahl von Argumenten in Microsoft RPC verwenden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2047"></span><span id="midl2047"></span><dl> <dt><strong>MIDL2047</strong></dt> </dl></td>
<td><dl> <dt><span id="named_parameter_cannot_be__void_"></span><span id="NAMED_PARAMETER_CANNOT_BE__VOID_"></span>Benannter Parameter darf nicht void sein &quot;&quot;</dt> <dd> Ein Parameter mit dem Basistyp <a href="void.md"><strong>void</strong></a> wird mit einem Namen angegeben.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2048"></span><span id="midl2048"></span><dl> <dt><strong>MIDL2048</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_derives_from__coclass__or__module_"></span><span id="PARAMETER_DERIVES_FROM__COCLASS__OR__MODULE_"></span>Parameter wird von &quot; coclass oder &quot; module &quot;&quot;</dt> <dd> Die <a href="coclass.md"><strong>Co-Klasse</strong></a> gibt ein Objekt der obersten Ebene an, das Schnittstellen und Disp-Schnittstellen enthält. Sie kann nicht als Parameter übergeben werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2049"></span><span id="midl2049"></span><dl> <dt><strong>MIDL2049</strong></dt> </dl></td>
<td><dl> <dt><span id="only_the_first_parameter_can_be_a_binding_handle__you_must_specify_the__ms_ext_switch"></span><span id="ONLY_THE_FIRST_PARAMETER_CAN_BE_A_BINDING_HANDLE__YOU_MUST_SPECIFY_THE__MS_EXT_SWITCH"></span>nur der erste Parameter kann ein Bindungshand handle sein. Sie müssen den Schalter /ms_ext angeben.</dt> <dd> DCE RPC lässt zu, dass nur der erste Parameter ein Bindungshandler ist. Beim Kompilieren mit dem <a href="-osf.md"><strong>Schalter /osf</strong></a> wird der standardmäßige <a href="-ms-ext.md"><strong>Schalter /ms_ext</strong></a> deaktiviert, der mehrere Handleparameter und Handleparameter an einer anderen Position als der linken Seite unterstützt.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2050"></span><span id="midl2050"></span><dl> <dt><strong>MIDL2050</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_use__comm_status__on_both_a_parameter_and_a_return_type"></span><span id="CANNOT_USE__COMM_STATUS__ON_BOTH_A_PARAMETER_AND_A_RETURN_TYPE"></span>[comm_status] kann nicht sowohl für einen Parameter als auch für einen Rückgabetyp verwendet werden.</dt> <dd> Sowohl die Prozedur als auch einer ihrer Parameter verfügen über das Attribut [<a href="comm-status.md"><strong>comm_status</strong></a>] . Das Attribut [<strong>comm_status</strong>] gibt an, dass nur ein Datenobjekt gleichzeitig vom Typ <a href="error-status-t.md"><strong>error_status_t.</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2051"></span><span id="midl2051"></span><dl> <dt><strong>MIDL2051</strong></dt> </dl></td>
<td><dl> <dt><span id="__local__attribute_on_a_procedure_requires__ms_ext"></span><span id="__LOCAL__ATTRIBUTE_ON_A_PROCEDURE_REQUIRES__MS_EXT"></span> Das Attribut [local] für eine Prozedur erfordert /ms_ext</dt> <dd> Das Attribut [<a href="local.md"><strong>local</strong></a>] ist eine Microsoft-Erweiterung für DCE-IDL. Um dieses Attribut für eine Funktion zu verwenden, können Sie nicht mit dem <a href="-osf.md"><strong>Schalter /osf kompilieren.</strong></a> Der <strong>Schalter /osf</strong> überschreibt die MIDL-Compiler-Standardschalter <a href="-ms-ext.md"><strong>/ms_ext</strong></a> und <a href="-c-ext.md"><strong>/c_ext.</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2052"></span><span id="midl2052"></span><dl> <dt><strong>MIDL2052</strong></dt> </dl></td>
<td><dl> <dt><span id="property_attributes_may_only_be_used_with_procedures"></span><span id="PROPERTY_ATTRIBUTES_MAY_ONLY_BE_USED_WITH_PROCEDURES"></span>Eigenschaftsattribute dürfen nur mit Prozeduren verwendet werden.</dt> <dd> Falsche Verwendung eines Attributs [<a href="propget.md"><strong>propget</strong></a>], [<a href="propput.md"><strong>propput</strong></a>] oder [<a href="propputref.md"><strong>propputref</strong></a>] . Stellen Sie sicher, dass Sie den Funktionsnamen der Eigenschaft richtig geschrieben haben und dass die Eigenschaft und die Funktion denselben Namen haben.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2053"></span><span id="midl2053"></span><dl> <dt><strong>MIDL2053</strong></dt> </dl></td>
<td><dl> <dt><span id="a_procedure_may_not_have_more_than_one_property_attribute"></span><span id="A_PROCEDURE_MAY_NOT_HAVE_MORE_THAN_ONE_PROPERTY_ATTRIBUTE"></span>Eine Prozedur darf nicht mehr als ein Eigenschaftsattribut haben.</dt> <dd> Für eine Funktion kann nur eines der Attribute [<a href="propget.md"><strong>propget</strong></a>], [<a href="propput.md"><strong>propput</strong></a>] oder [<a href="propputref.md"><strong>propputref</strong></a>] angegeben werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2054"></span><span id="midl2054"></span><dl> <dt><strong>MIDL2054</strong></dt> </dl></td>
<td><dl> <dt><span id="the_procedure_has_an_illegal_combination_of_operation_attributes"></span><span id="THE_PROCEDURE_HAS_AN_ILLEGAL_COMBINATION_OF_OPERATION_ATTRIBUTES"></span>Die Prozedur verfügt über eine unzulässige Kombination von Vorgangsattributen.</dt> <dd> Bestimmte Attribute können nicht in Verbindung mit anderen Attributen verwendet werden. Überprüfen Sie die MIDL-Sprachreferenz auf die genauen Anforderungen und die Syntax der in diesem Verfahren verwendeten Attribute.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2055"></span><span id="midl2055"></span><dl> <dt><strong>MIDL2055</strong></dt> </dl></td>
<td><dl> <dt><span id="field_deriving_from_a_conformant_array_must_be_the_last_member_of_the_structure"></span><span id="FIELD_DERIVING_FROM_A_CONFORMANT_ARRAY_MUST_BE_THE_LAST_MEMBER_OF_THE_STRUCTURE"></span>Das von einem konformen Array ableitende Feld muss das letzte Member der Struktur sein.</dt> <dd> Die -Struktur enthält ein konformes Array, das nicht das letzte Element in der -Struktur ist. Das konforme Array muss als letztes Strukturelement angezeigt werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2056"></span><span id="midl2056"></span><dl> <dt><strong>MIDL2056</strong></dt> </dl></td>
<td><dl> <dt><span id="duplicate__case__label"></span><span id="DUPLICATE__CASE__LABEL"></span>Doppelte [Case]-Bezeichnung</dt> <dd> Es wurde eine Doppelte Case-Bezeichnung angegeben. Die doppelte Bezeichnung wird angezeigt.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2057"></span><span id="midl2057"></span><dl> <dt><strong>MIDL2057</strong></dt> </dl></td>
<td><dl> <dt><span id="no__default__case_specified_for_discriminated_union"></span><span id="NO__DEFAULT__CASE_SPECIFIED_FOR_DISCRIMINATED_UNION"></span>Kein [Standard]-Fall für Unterscheidungs-Union angegeben</dt> <dd> Eine Unterscheidungs-Union wurde ohne Standardfall angegeben.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2058"></span><span id="midl2058"></span><dl> <dt><strong>MIDL2058</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_expression_cannot_be_resolved"></span><span id="ATTRIBUTE_EXPRESSION_CANNOT_BE_RESOLVED"></span>Attributausdruck kann nicht aufgelöst werden</dt> <dd> Der dem Attribut zugeordnete Ausdruck kann nicht aufgelöst werden. Dieser Fehler tritt normalerweise auf, wenn eine variable, die im Ausdruck angezeigt wird, nicht definiert ist. Der Fehler kann beispielsweise auftreten, wenn die Variable <em>s</em> nicht definiert ist und vom Attribut [ size_is ]<a href="size-is.md"><strong>verwendet wird.</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2059"></span><span id="midl2059"></span><dl> <dt><strong>MIDL2059</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_expression_must_be_of_integral_type__no_support_for_64-bit_expressions"></span><span id="ATTRIBUTE_EXPRESSION_MUST_BE_OF_INTEGRAL_TYPE__NO_SUPPORT_FOR_64-BIT_EXPRESSIONS"></span>Attributausdruck muss vom ganzzahlig Typ sein, keine Unterstützung für 64-Bit-Ausdrücke</dt> <dd> Die angegebene Attributvariable oder der angegebene Ausdruck muss ein ganzzahlder Typ sein. Dieser Fehler tritt auf, wenn der Attributausdruckstyp nicht in eine ganze Zahl auflöset.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2060"></span><span id="midl2060"></span><dl> <dt><strong>MIDL2060</strong></dt> </dl></td>
<td><dl> <dt><span id="_byte_count__requires__ms_ext"></span><span id="_BYTE_COUNT__REQUIRES__MS_EXT"></span>[byte_count] erfordert /ms_ext</dt> <dd> Das Attribut [<a href="byte-count.md"><strong>byte_count</strong></a>] ist eine Microsoft-Erweiterung für DCE-IDL. Um dieses Attribut zu verwenden, können Sie nicht mit dem <a href="-osf.md"><strong>Schalter /osf</strong></a> kompilieren, der die MIDL-Compiler-Standardschalter <a href="-ms-ext.md"><strong>/ms_ext</strong></a> <a href="-c-ext.md"><strong>und /c_ext.</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2061"></span><span id="midl2061"></span><dl> <dt><strong>MIDL2061</strong></dt> </dl></td>
<td><dl> <dt><span id="_byte_count__can_be_applied_only_to_out_parameters_of_pointer_type"></span><span id="_BYTE_COUNT__CAN_BE_APPLIED_ONLY_TO_OUT_PARAMETERS_OF_POINTER_TYPE"></span>[byte_count] kann nur auf out-Parameter des Zeigertyps angewendet werden.</dt> <dd> Das [<a href="byte-count.md"><strong>byte_count</strong></a>] -Attribut kann nur auf [<a href="out-idl.md"><strong>out</strong></a>] -Parameter angewendet werden, und alle [<strong>out</strong>]-Parameter müssen Zeigertypen sein.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2062"></span><span id="midl2062"></span><dl> <dt><strong>MIDL2062</strong></dt> </dl></td>
<td><dl> <dt><span id="_byte_count__cannot_be_specified_on_a_pointer_to_a_conformant_array_or_structure"></span><span id="_BYTE_COUNT__CANNOT_BE_SPECIFIED_ON_A_POINTER_TO_A_CONFORMANT_ARRAY_OR_STRUCTURE"></span>[byte_count] kann nicht für einen Zeiger auf ein konformes Array oder eine konforme Struktur angegeben werden.</dt> <dd> Das Attribut [<a href="byte-count.md"><strong>byte_count</strong></a>] kann nicht auf ein konformes Array oder eine konforme Struktur angewendet werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2063"></span><span id="midl2063"></span><dl> <dt><strong>MIDL2063</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_specifying_the_byte_count_is_not__in__only_or_byte_count_parameter_is_not__out__only"></span><span id="PARAMETER_SPECIFYING_THE_BYTE_COUNT_IS_NOT__IN__ONLY_OR_BYTE_COUNT_PARAMETER_IS_NOT__OUT__ONLY"></span>Parameter, der die Byteanzahl angibt, ist nicht nur [in] oder der Byteanzahlparameter ist nicht nur [out]</dt> <dd> Der wert, der dem<a href="byte-count.md"><strong>[byte_count</strong></a>] zugeordnet ist, muss vom Client an den Server übertragen werden. es muss ein<a href="in.md"><strong>[in</strong></a>] -Parameter sein. Der<strong>[byte_count</strong>] -Parameter muss kein [<strong>in, out ] -Parameter</strong>sein.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2064"></span><span id="midl2064"></span><dl> <dt><strong>MIDL2064</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_specifying_the_byte_count_is_not_an_integral_type"></span><span id="PARAMETER_SPECIFYING_THE_BYTE_COUNT_IS_NOT_AN_INTEGRAL_TYPE"></span>Der Parameter, der die Byteanzahl angibt, ist kein integraler Typ.</dt> <dd> Der wert, der der Byteanzahl zugeordnet ist, muss der ganzzahlige <a href="int.md"><strong>Typ int,</strong></a> <a href="small.md"><strong>small,</strong></a> <a href="short.md"><strong>short</strong></a>oder <a href="long.md"><strong>long sein.</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2065"></span><span id="midl2065"></span><dl> <dt><strong>MIDL2065</strong></dt> </dl></td>
<td><dl> <dt><span id="_byte_count__cannot_be_specified_on_a_parameter_with_size_attributes"></span><span id="_BYTE_COUNT__CANNOT_BE_SPECIFIED_ON_A_PARAMETER_WITH_SIZE_ATTRIBUTES"></span>[byte_count] kann nicht für einen Parameter mit Größenattributen angegeben werden.</dt> <dd> Das Attribut [<a href="byte-count.md"><strong>byte_count</strong></a>] kann nicht mit anderen Größenattributen wie [<a href="size-is.md"><strong>size_is</strong></a>] oder [ length_is ]<a href="length-is.md"><strong>verwendet werden.</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2066"></span><span id="midl2066"></span><dl> <dt><strong>MIDL2066</strong></dt> </dl></td>
<td><dl> <dt><span id="_case__expression_is_not_constant"></span><span id="_CASE__EXPRESSION_IS_NOT_CONSTANT"></span>[case]-Ausdruck ist nicht konstant</dt> <dd> Der für die Case-Bezeichnung angegebene Ausdruck ist keine Konstante.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2067"></span><span id="midl2067"></span><dl> <dt><strong>MIDL2067</strong></dt> </dl></td>
<td><dl> <dt><span id="_case__expression_is_not_of_integral_type"></span><span id="_CASE__EXPRESSION_IS_NOT_OF_INTEGRAL_TYPE"></span>[case]-Ausdruck ist nicht vom integralen Typ</dt> <dd> Der für die Case-Bezeichnung angegebene Ausdruck ist kein ganzzahliger Typ.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2068"></span><span id="midl2068"></span><dl> <dt><strong>MIDL2068</strong></dt> </dl></td>
<td><dl> <dt><span id="specifying__context_handle__on_a_type_other_than_void___requires__ms_ext"></span><span id="SPECIFYING__CONTEXT_HANDLE__ON_A_TYPE_OTHER_THAN_VOID___REQUIRES__MS_EXT"></span>Die Angabe von [context_handle] für einen anderen Typ als void * erfordert /ms_ext</dt> <dd> Für die DCE-RPC-Kompatibilität muss das Kontexthandler ein Zeiger vom Typ <strong>void * sein.</strong> Wenn die Kontexthandles anderen Typen als <strong>void *</strong>zugeordnet werden sollen, verwenden Sie nicht den MIDL-Compilerschalter <a href="-osf.md"><strong>/osf,</strong></a>der den MIDL-Compiler-Standardschalter <a href="-ms-ext.md"><strong>/ms_ext.</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2069"></span><span id="midl2069"></span><dl> <dt><strong>MIDL2069</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_specify_more_than_one_parameter_with_each_of_comm_status_fault_status"></span><span id="CANNOT_SPECIFY_MORE_THAN_ONE_PARAMETER_WITH_EACH_OF_COMM_STATUS_FAULT_STATUS"></span>kann nicht mehr als einen Parameter mit jedem comm_status/fault_status</dt> <dd> Eine Prozedur kann nur einen Parameter mit dem Attribut [<a href="comm-status.md"><strong>comm_status</strong></a>] haben. Es kann nur einen Parameter mit dem Attribut [<a href="fault-status.md"><strong>fault_status</strong></a>] haben.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2070"></span><span id="midl2070"></span><dl> <dt><strong>MIDL2070</strong></dt> </dl></td>
<td><dl> <dt><span id="comm_status_fault_status_parameter_must_be_an__out__only_pointer_parameter"></span><span id="COMM_STATUS_FAULT_STATUS_PARAMETER_MUST_BE_AN__OUT__ONLY_POINTER_PARAMETER"></span>comm_status/fault_status Parameter muss nur ein [out]-Zeigerparameter sein.</dt> <dd> Die Fehlercodetypen [<a href="comm-status.md"><strong>comm_status</strong></a>] und [<a href="fault-status.md"><strong>fault_status</strong></a>] werden vom Server an den Client übertragen und müssen daher als [<a href="out-idl.md"><strong>out</strong></a>]-Parameter angegeben werden. Aufgrund der Einschränkungen in der Programmiersprache C müssen alle<strong>[out]-Parameter</strong>Zeiger sein.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2071"></span><span id="midl2071"></span><dl> <dt><strong>MIDL2071</strong></dt> </dl></td>
<td><dl> <dt><span id="endpoint_syntax_error"></span><span id="ENDPOINT_SYNTAX_ERROR"></span>Endpunktsyntaxfehler</dt> <dd> Die Endpunktsyntax ist falsch.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2072"></span><span id="midl2072"></span><dl> <dt><strong>MIDL2072</strong></dt> </dl></td>
<td><dl> <dt><span id="inapplicable_attribute"></span><span id="INAPPLICABLE_ATTRIBUTE"></span>Inapplicable-Attribut</dt> <dd> Das angegebene Attribut kann in diesem Konstrukt nicht angewendet werden. Das Zeichenfolgenattribut gilt beispielsweise für <a href="char-idl.md"><strong>char-Arrays</strong></a> oder <strong>char-Zeiger</strong> und kann nicht auf eine Struktur angewendet werden, die aus zwei kurzen <a href="short.md"><strong>ganzen</strong></a> Zahlen besteht: <br/>
<pre class="syntax" data-space="preserve"><code>typedef [string] struct moo 
{
    short x;
    short y;
};</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2073"></span><span id="midl2073"></span><dl> <dt><strong>MIDL2073</strong></dt> </dl></td>
<td><dl> <dt><span id="_allocate__requires__ms_ext"></span><span id="_ALLOCATE__REQUIRES__MS_EXT"></span>[allocate] erfordert /ms_ext</dt> <dd> Das <a href="allocate.md"><strong>Attribut allocate</strong></a> stellt eine Microsoft-Erweiterung dar, die nicht als Teil von DCE RPC definiert ist. Um dieses Attribut zu verwenden, können Sie nicht mit dem <a href="-osf.md"><strong>Schalter /osf</strong></a> kompilieren, der den MIDL-Compiler-Standardschalter <a href="-ms-ext.md"><strong>/ms_ext</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2074"></span><span id="midl2074"></span><dl> <dt><strong>MIDL2074</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid__allocate__mode"></span><span id="INVALID__ALLOCATE__MODE"></span>Ungültiger [allocate]-Modus</dt> <dd> Für das Attributkonstrukt<a href="allocate.md"><strong>[allocate</strong></a>] wurde ein ungültiger Modus angegeben. Die vier gültigen Modi sind single_node, all_nodes, on_null und immer.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2075"></span><span id="midl2075"></span><dl> <dt><strong>MIDL2075</strong></dt> </dl></td>
<td><dl> <dt><span id="length_attributes_cannot_be_applied_with_string_attribute"></span><span id="LENGTH_ATTRIBUTES_CANNOT_BE_APPLIED_WITH_STRING_ATTRIBUTE"></span>Längenattribute können nicht mit Zeichenfolgenattribut angewendet werden</dt> <dd> Wenn das Zeichenfolgenattribut verwendet wird, rufen die generierten Stubdateien die <strong>strlen-Funktion</strong> auf, um die Zeichenfolgenlänge zu bestimmen. Verwenden Sie nicht das length-Attribut und das Zeichenfolgenattribut für dieselbe Variable.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2076"></span><span id="midl2076"></span><dl> <dt><strong>MIDL2076</strong></dt> </dl></td>
<td><dl> <dt><span id="_last_is__and__length_is__cannot_be_specified_at_the_same_time"></span><span id="_LAST_IS__AND__LENGTH_IS__CANNOT_BE_SPECIFIED_AT_THE_SAME_TIME"></span>[last_is] und [length_is] können nicht gleichzeitig angegeben werden.</dt> <dd> Sowohl [<a href="last-is.md"><strong>last_is</strong></a>] als auch [<a href="length-is.md"><strong>length_is</strong></a>] wurden für dasselbe Array angegeben. Diese Attribute sind wie folgt verknüpft: length = last first + 1. Da jeder Wert von dem anderen abgeleitet werden kann, geben Sie nicht beides an.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2077"></span><span id="midl2077"></span><dl> <dt><strong>MIDL2077</strong></dt> </dl></td>
<td><dl> <dt><span id="_max_is__and__size_is__cannot_be_specified_at_the_same_time"></span><span id="_MAX_IS__AND__SIZE_IS__CANNOT_BE_SPECIFIED_AT_THE_SAME_TIME"></span>[max_is] und [size_is] können nicht gleichzeitig angegeben werden.</dt> <dd> Sowohl [ <a href="max-is.md"><strong>max_is</strong></a>] als auch [ <a href="size-is.md"><strong>size_is</strong></a>] wurden für dasselbe Array angegeben. Diese Attribute sind wie folgt verknüpft: max = size + 1. Da jeder Wert von dem anderen abgeleitet werden kann, geben Sie nicht beides an.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2078"></span><span id="midl2078"></span><dl> <dt><strong>MIDL2078</strong></dt> </dl></td>
<td><dl> <dt><span id="no__switch_is__attribute_specified_at_use_of_union"></span><span id="NO__SWITCH_IS__ATTRIBUTE_SPECIFIED_AT_USE_OF_UNION"></span>Kein [switch_is]-Attribut bei Verwendung von union angegeben</dt> <dd> Für die Union wurde keine Diskriminanz angegeben. Das Attribut [<a href="switch-is.md"><strong>switch_is</strong></a>] gibt die Diskriminanz an, die zum Auswählen zwischen den Union-Feldern verwendet wird.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2079"></span><span id="midl2079"></span><dl> <dt><strong>MIDL2079</strong></dt> </dl></td>
<td><dl> <dt><span id="no__uuid__specified"></span><span id="NO__UUID__SPECIFIED"></span>kein [uuid] angegeben</dt> <dd> Für die Schnittstelle wurde keine UUID angegeben.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2080"></span><span id="midl2080"></span><dl> <dt><strong>MIDL2080</strong></dt> </dl></td>
<td><dl> <dt><span id="_uuid__ignored_on__local__interface"></span><span id="_UUID__IGNORED_ON__LOCAL__INTERFACE"></span>[uuid] für [local]-Schnittstelle ignoriert</dt> <dd> Die Verwendung des Attributs [<a href="local.md"><strong>local</strong></a>] für eine Objektschnittstelle bewirkt, dass der MIDL-Compiler das<a href="uuid.md"><strong>[uuid]-Attribut</strong></a>ignoriert. Sie können nicht beide Attribute für eine RPC-Schnittstelle verwenden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2081"></span><span id="midl2081"></span><dl> <dt><strong>MIDL2081</strong></dt> </dl></td>
<td><dl> <dt><span id="type_mismatch_between_length_and_size_attribute_expressions"></span><span id="TYPE_MISMATCH_BETWEEN_LENGTH_AND_SIZE_ATTRIBUTE_EXPRESSIONS"></span>Typkonflikt zwischen Längen- und Größenattributausdrücken</dt> <dd> Die Längen- und Größenattributausdrücke müssen dieselben Typen aufweisen. Diese Warnung wird beispielsweise ausgegeben, wenn die Attributvariable für den<a href="size-is.md"><strong>[size_is]-Ausdruck</strong></a>vom Typ <strong>unsigned long</strong> und die Attributvariable für den Ausdruck [<a href="length-is.md"><strong>length_is</strong></a>] vom Typ <a href="long.md"><strong>long</strong></a>ist.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2082"></span><span id="midl2082"></span><dl> <dt><strong>MIDL2082</strong></dt> </dl></td>
<td><dl> <dt><span id="_string__attribute_must_be_specified__byte____char___or__wchar_t__array_or_pointer"></span><span id="_STRING__ATTRIBUTE_MUST_BE_SPECIFIED__BYTE____CHAR___OR__WCHAR_T__ARRAY_OR_POINTER"></span>Das [String]-Attribut muss &quot; byte, &quot; &quot; char oder wchar_t Array &quot; oder &quot; &quot; Zeiger angegeben werden.</dt> <dd> Ein Zeichenfolgenattribut kann nicht auf einen Zeiger oder ein Array angewendet werden, dessen Basistyp keine <a href="byte.md"><strong>Byte-,</strong></a> <a href="char-idl.md"><strong>char-</strong></a>oder <a href="struct.md"><strong>-Struktur</strong></a> ist, in der die Member alle vom <strong>Byte-</strong> oder <strong>Char-Typ</strong> sind.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2083"></span><span id="midl2083"></span><dl> <dt><strong>MIDL2083</strong></dt> </dl></td>
<td><dl> <dt><span id="mismatch_between_the_type_of_the__switch_is__expression_and_the_switch_type_of_the_union"></span><span id="MISMATCH_BETWEEN_THE_TYPE_OF_THE__SWITCH_IS__EXPRESSION_AND_THE_SWITCH_TYPE_OF_THE_UNION"></span>Konflikt zwischen dem Typ des [switch_is]-Ausdrucks und dem Switchtyp der Union</dt> <dd> Wenn die Union [<a href="switch-type.md"><strong>switch_type</strong></a>] nicht angegeben ist, entspricht der Switchtyp dem Feld [<a href="switch-is.md"><strong>switch_is</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2084"></span><span id="midl2084"></span><dl> <dt><strong>MIDL2084</strong></dt> </dl></td>
<td><dl> <dt><span id="_transmit_as__must_not_be_applied_to_a_type_that_derives_from_a_context_handle"></span><span id="_TRANSMIT_AS__MUST_NOT_BE_APPLIED_TO_A_TYPE_THAT_DERIVES_FROM_A_CONTEXT_HANDLE"></span>[transmit_as] darf nicht auf einen Typ angewendet werden, der von einem Kontexthandle abgeleitet wird.</dt> <dd> Kontexthandles können nicht als andere Typen übertragen werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2085"></span><span id="midl2085"></span><dl> <dt><strong>MIDL2085</strong></dt> </dl></td>
<td><dl> <dt><span id="_transmit_as__must_specify_a_transmissible_type"></span><span id="_TRANSMIT_AS__MUST_SPECIFY_A_TRANSMISSIBLE_TYPE"></span>[transmit_as] muss einen transkahenten Typ angeben.</dt> <dd> Der angegebene Typ [<a href="transmit-as.md"><strong>transmit_as</strong></a>] wird von einem Typ abgeleitet, der nicht von Microsoft RPC übertragen werden kann, z. B. <a href="void.md"><strong>void</strong></a>, <strong>void *</strong>oder <a href="int.md"><strong>int</strong></a>. Verwenden Sie einen definierten RPC-Basistyp. Fügen Sie im Fall von <strong>int</strong>Größenspezifizierer wie <a href="small.md"><strong>small</strong></a>, <a href="short.md"><strong>short</strong></a>oder <a href="long.md"><strong>long</strong></a> hinzu, um den <strong>wertigen</strong>zu qualifizieren.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2086"></span><span id="midl2086"></span><dl> <dt><strong>MIDL2086</strong></dt> </dl></td>
<td><dl> <dt><span id="transmitted_type_for__transmit_as__and__represent_as__must_not_be_a_pointer_or_derive_from_a_pointer"></span><span id="TRANSMITTED_TYPE_FOR__TRANSMIT_AS__AND__REPRESENT_AS__MUST_NOT_BE_A_POINTER_OR_DERIVE_FROM_A_POINTER"></span>Der übertragene Typ für [transmit_as] und [represent_as] darf kein Zeiger sein oder von einem Zeiger abgeleitet sein.</dt> <dd> Der übertragene Typ kann kein Zeiger sein oder von einem Zeiger abgeleitet werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2087"></span><span id="midl2087"></span><dl> <dt><strong>MIDL2087</strong></dt> </dl></td>
<td><dl> <dt><span id="presented_type_for__transmit_as__and__represent_as__must_not_derive_from_a_conformant_varying_array__its_pointer_equivalent__or_a_conformant_varying_structure"></span><span id="PRESENTED_TYPE_FOR__TRANSMIT_AS__AND__REPRESENT_AS__MUST_NOT_DERIVE_FROM_A_CONFORMANT_VARYING_ARRAY__ITS_POINTER_EQUIVALENT__OR_A_CONFORMANT_VARYING_STRUCTURE"></span>Der dargestellte Typ für [transmit_as] und [represent_as] darf nicht von einem konformen/variierenden Array, seiner Zeigerentsprechung oder einer konformen/variierenden Struktur abgeleitet werden.</dt> <dd> Der Typ, auf den [<a href="transmit-as.md"><strong>transmit_as</strong></a>] angewendet wurde, kann nicht von einem konformen Array oder einer konformen Struktur abgeleitet werden (einem Array oder einer Struktur, dessen Größe zur Laufzeit bestimmt wird).<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2088"></span><span id="midl2088"></span><dl> <dt><strong>MIDL2088</strong></dt> </dl></td>
<td><dl> <dt><span id="_uuid__format_is_incorrect"></span><span id="_UUID__FORMAT_IS_INCORRECT"></span>[uuid] Format ist falsch</dt> <dd> Das UUID-Format entspricht nicht der Spezifikation. Die UUID muss eine Zeichenfolge sein, die aus fünf Sequenzen von Hexadezimalziffern der Länge 8, 4, 4, 4 und 12 Ziffern besteht. &quot;12345678-1234-ABCD-EF01-28A49C28F17D &quot; ist eine gültige UUID. Verwenden Sie die Funktion <a href="/windows/desktop/api/rpcdce/nf-rpcdce-uuidcreate"><strong>UuidCreate</strong></a> oder ein Hilfsprogramm, um eine gültige UUID zu generieren.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2089"></span><span id="midl2089"></span><dl> <dt><strong>MIDL2089</strong></dt> </dl></td>
<td><dl> <dt><span id="uuid_is_not_a_hexadecimal_number"></span><span id="UUID_IS_NOT_A_HEXADECIMAL_NUMBER"></span>uuid ist keine Hexadezimalzahl</dt> <dd> Die für die Schnittstelle angegebene UUID enthält Zeichen, die in einer Hexadezimalzahlendarstellung ungültig sind. Die Zeichen 0 bis 9 und A bis F sind in einer hexadezimalen Darstellung gültig.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2090"></span><span id="midl2090"></span><dl> <dt><strong>MIDL2090</strong></dt> </dl></td>
<td><dl> <dt><span id="optional_parameters_must_come_after_required_parameters"></span><span id="OPTIONAL_PARAMETERS_MUST_COME_AFTER_REQUIRED_PARAMETERS"></span>Optionale Parameter müssen nach den erforderlichen Parametern angegeben werden.</dt> <dd> Eine Beschreibung der Reihenfolge von Parameterlisten finden Sie unter [<a href="optional.md"><strong>optional</strong></a>] in der MIDL-Sprachreferenz.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2091"></span><span id="midl2091"></span><dl> <dt><strong>MIDL2091</strong></dt> </dl></td>
<td><dl> <dt><span id="_dllname__required_when__entry__is_used"></span><span id="_DLLNAME__REQUIRED_WHEN__ENTRY__IS_USED"></span>[dllname] erforderlich, wenn [entry] verwendet wird</dt> <dd> Wenn Sie einen Einstiegspunkt in eine DLL angeben, müssen Sie auch den Namen dieser DLL mithilfe des Attributs [<a href="dllname-str-.md"><strong>dllname</strong></a>] angeben.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2092"></span><span id="midl2092"></span><dl> <dt><strong>MIDL2092</strong></dt> </dl></td>
<td><dl> <dt><span id="_bindable__is_invalid_without__propget____propput___or__propputref_"></span><span id="_BINDABLE__IS_INVALID_WITHOUT__PROPGET____PROPPUT___OR__PROPPUTREF_"></span>[bindbar] ist ohne [propget], [propput] oder [propputref] ungültig.</dt> <dd> Das<a href="bindable.md"><strong>[bindbare</strong></a>] -Attribut ist nur für eine Eigenschaft gültig. Daher müssen Sie auch eine der Eigenschaftenzugriffsfunktionen oder Eigenschafteneinstellungsfunktionen angeben.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2093"></span><span id="midl2093"></span><dl> <dt><strong>MIDL2093</strong></dt> </dl></td>
<td><dl> <dt><span id="procedures_with__propput__or__propputref__must_have_at_least_one_parameter"></span><span id="PROCEDURES_WITH__PROPPUT__OR__PROPPUTREF__MUST_HAVE_AT_LEAST_ONE_PARAMETER"></span>Prozeduren mit [propput] oder [propputref] müssen mindestens einen Parameter aufweisen.</dt> <dd> Eine<a href="propput.md"><strong>[propput]-</strong></a>oder [ <a href="propputref.md"><strong>propputref]-Prozedur</strong></a>muss mindestens einen<a href="in.md"><strong>[in</strong></a>]-Parameter mit der festzulegenden Eigenschaft aufweisen. Eine<a href="propget.md"><strong>[propget]-Prozedur</strong></a>muss mindestens einen<a href="out-idl.md"><strong>[out-,</strong></a> <a href="retval.md"><strong>retval</strong></a>]-Parameter aufweisen, um die Eigenschaft oder den Verweis zu empfangen.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2094"></span><span id="midl2094"></span><dl> <dt><strong>MIDL2094</strong></dt> </dl></td>
<td><dl> <dt><span id="_id__attribute_is_required"></span><span id="_ID__ATTRIBUTE_IS_REQUIRED"></span>[id]-Attribut ist erforderlich</dt> <dd> Diese Memberfunktion erfordert aufgrund der verwendeten <a href="dispinterface.md"><strong>dispinterface-Syntax</strong></a> eine DISPID, die Sie mithilfe des Attributs [ <a href="id.md"><strong>id</strong></a>] angeben. Wenn Sie eine <strong>Disp-Schnittstelle</strong> mithilfe von Eigenschaften und Methoden angeben, müssen Sie eine DISPID für jede Eigenschaft und Methode angeben.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2095"></span><span id="midl2095"></span><dl> <dt><strong>MIDL2095</strong></dt> </dl></td>
<td><dl> <dt><span id="interface_name_specified_in_the_ACF_does_not_match_that_specified_in_the_IDL_file"></span><span id="interface_name_specified_in_the_acf_does_not_match_that_specified_in_the_idl_file"></span><span id="INTERFACE_NAME_SPECIFIED_IN_THE_ACF_DOES_NOT_MATCH_THAT_SPECIFIED_IN_THE_IDL_FILE"></span>Der im ACF angegebene Schnittstellenname stimmt nicht mit dem in der IDL-Datei angegebenen Schnittstellennamen überein.</dt> <dd> Im aktuellen Compilermodus muss der Name, der dem Schnittstellenschlüsselwort in der ACF folgt, mit dem Namen identisch sein, der auf das Schnittstellenschlüsselwort in der IDL-Datei folgt. Die Schnittstellennamen in den IDL- und ACF-Dateien können sich unterscheiden, wenn Sie mit dem MIDL-Compilerschalter <a href="-acf.md"><strong>/acf</strong></a>kompilieren.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2096"></span><span id="midl2096"></span><dl> <dt><strong>MIDL2096</strong></dt> </dl></td>
<td><dl> <dt><span id="duplicated_attribute"></span><span id="DUPLICATED_ATTRIBUTE"></span>Dupliziertes Attribut</dt> <dd> Doppelte oder in Konflikt stehende Attribute wurden angegeben. Dieser Fehler tritt häufig auf, wenn sich zwei Attribute gegenseitig ausschließen. Beispielsweise können die Attribute [<a href="code.md"><strong>code</strong></a>] und [<a href="nocode.md"><strong>nocode</strong></a>] nicht gleichzeitig verwendet werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2097"></span><span id="midl2097"></span><dl> <dt><strong>MIDL2097</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_with__comm_status__or__fault_status__attribute_must_be_a_pointer_to_type_error_status_t"></span><span id="PARAMETER_WITH__COMM_STATUS__OR__FAULT_STATUS__ATTRIBUTE_MUST_BE_A_POINTER_TO_TYPE_ERROR_STATUS_T"></span>parameter with [comm_status] or [fault_status] attribute must be a pointer to type error_status_t</dt> <dd> Wenn [<a href="fault-status.md"><strong>fault_status</strong></a>] oder [<a href="comm-status.md"><strong>comm_status</strong></a>] als Parameterattribut verwendet wird, muss der Parameter ein<a href="out-idl.md"><strong>[out]-Parameter</strong></a>vom Typ <a href="error-status-t.md"><strong>error_status_t</strong></a>sein. Wenn ein Serverfehler auftritt, wird der -Parameter auf den Fehlercode festgelegt. Wenn der Remoteaufruf erfolgreich abgeschlossen wurde, legt die Prozedur den Wert fest.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2098"></span><span id="midl2098"></span><dl> <dt><strong>MIDL2098</strong></dt> </dl></td>
<td><dl> <dt><span id="a__local__procedure_cannot_be_specified_in_ACF_file"></span><span id="a__local__procedure_cannot_be_specified_in_acf_file"></span><span id="A__LOCAL__PROCEDURE_CANNOT_BE_SPECIFIED_IN_ACF_FILE"></span>Eine [lokale] Prozedur kann nicht in der ACF-Datei angegeben werden.</dt> <dd> Im ACF wurde eine lokale Prozedur angegeben. Die lokale Prozedur kann nur in der IDL-Datei angegeben werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2099"></span><span id="midl2099"></span><dl> <dt><strong>MIDL2099</strong></dt> </dl></td>
<td><dl> <dt><span id="specified_type_is_not_defined_as_a_handle"></span><span id="SPECIFIED_TYPE_IS_NOT_DEFINED_AS_A_HANDLE"></span>Der angegebene Typ ist nicht als Handle definiert.</dt> <dd> Der im Attribut [<a href="implicit-handle.md"><strong>implicit_handle</strong></a>] angegebene Typ ist nicht als Handletyp definiert. Ändern Sie die Typdefinition oder den vom Attribut angegebenen Typnamen.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2100"></span><span id="midl2100"></span><dl> <dt><strong>MIDL2100</strong></dt> </dl></td>
<td><dl> <dt><span id="procedure_undefined"></span><span id="PROCEDURE_UNDEFINED"></span>prozedur undefined</dt> <dd> Ein Attribut wurde auf eine Prozedur im ACF angewendet, und diese Prozedur ist in der IDL-Datei nicht definiert.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2101"></span><span id="midl2101"></span><dl> <dt><strong>MIDL2101</strong></dt> </dl></td>
<td><dl> <dt><span id="this_parameter_does_not_exist_in_the_IDL_file"></span><span id="this_parameter_does_not_exist_in_the_idl_file"></span><span id="THIS_PARAMETER_DOES_NOT_EXIST_IN_THE_IDL_FILE"></span>Dieser Parameter ist in der IDL-Datei nicht vorhanden.</dt> <dd> Ein im ACF angegebener Parameter ist in der Definition in der IDL-Datei nicht vorhanden. Alle Parameter, Funktionen und Typdefinitionen, die im ACF angezeigt werden, müssen Parametern, Funktionen und Typen entsprechen, die zuvor in der IDL-Datei definiert wurden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2102"></span><span id="midl2102"></span><dl> <dt><strong>MIDL2102</strong></dt> </dl></td>
<td><dl> <dt><span id="this_array-bounds_construct_is_not_supported"></span><span id="THIS_ARRAY-BOUNDS_CONSTRUCT_IS_NOT_SUPPORTED"></span>Dieses arraygebundene Konstrukt wird nicht unterstützt.</dt> <dd> MIDL unterstützt derzeit das Ausdrücken der oberen und unteren Begrenzung eines Arrays in der Form Array[Lower .. Upper] nur, wenn die Konstante, die die untere Grenze des Arrays angibt, in den Wert 0 (null) auflöset.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2103"></span><span id="midl2103"></span><dl> <dt><strong>MIDL2103</strong></dt> </dl></td>
<td><dl> <dt><span id="array_bound_specification_is_illegal"></span><span id="ARRAY_BOUND_SPECIFICATION_IS_ILLEGAL"></span>Arraygebundene Spezifikation ist ungültig</dt> <dd> Die Benutzerspezifikation von Array-Begrenzungen für das Array fester Größe ist ungültig. Beispiel: <br/>
<pre class="syntax" data-space="preserve"><code>typedef short Array[-1]</code></pre>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2104"></span><span id="midl2104"></span><dl> <dt><strong>MIDL2104</strong></dt> </dl></td>
<td><dl> <dt><span id="pointer_to_a_conformant_array_or_an_array_that_contains_a_conformant_array_is_not_supported"></span><span id="POINTER_TO_A_CONFORMANT_ARRAY_OR_AN_ARRAY_THAT_CONTAINS_A_CONFORMANT_ARRAY_IS_NOT_SUPPORTED"></span>Zeiger auf ein konformes Array oder ein Array, das ein konformes Array enthält, wird nicht unterstützt.</dt> <dd> Ungültige konforme Arrayverwendung. Regeln für konforme Arrays finden Sie unter <a href="/windows/desktop/Rpc/arrays-and-rpc">Arrays und RPC.</a><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2105"></span><span id="midl2105"></span><dl> <dt><strong>MIDL2105</strong></dt> </dl></td>
<td><dl> <dt><span id="pointee_array_does_not_derive_any_size"></span><span id="POINTEE_ARRAY_DOES_NOT_DERIVE_ANY_SIZE"></span>Pointee/Array leitet keine Größe ab</dt> <dd> Ein konformes Array wurde ohne Größenangabe angegeben. Sie können die Größe mit dem Attribut [<a href="max-is.md"><strong>max_is</strong></a>] oder [<a href="size-is.md"><strong>size_is</strong></a>] angeben.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2106"></span><span id="midl2106"></span><dl> <dt><strong>MIDL2106</strong></dt> </dl></td>
<td><dl> <dt><span id="only_fixed_arrays_and_SAFEARRAYs_are_legal_in_a_type_library"></span><span id="only_fixed_arrays_and_safearrays_are_legal_in_a_type_library"></span><span id="ONLY_FIXED_ARRAYS_AND_SAFEARRAYS_ARE_LEGAL_IN_A_TYPE_LIBRARY"></span>Nur feste Arrays und SAFEARRAYs sind in einer Typbibliothek legal.</dt> <dd> Sie haben einen Arraytyp in einer Bibliotheks-Anweisung verwendet, der nicht in einer Typbibliothek verwendet werden kann.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2107"></span><span id="midl2107"></span><dl> <dt><strong>MIDL2107</strong></dt> </dl></td>
<td><dl> <dt><span id="SAFEARRAYs_are_only_legal_inside_a_library_block"></span><span id="safearrays_are_only_legal_inside_a_library_block"></span><span id="SAFEARRAYS_ARE_ONLY_LEGAL_INSIDE_A_LIBRARY_BLOCK"></span>SAFEARRAYs sind nur innerhalb eines Bibliotheksblocks legal.</dt> <dd> Der MIDL-Compiler erkennt SAFEARRAY nur beim Generieren einer Typbibliothek als gültigen Datentyp.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2108"></span><span id="midl2108"></span><dl> <dt><strong>MIDL2108</strong></dt> </dl></td>
<td><dl> <dt><span id="badly_formed_character_constant"></span><span id="BADLY_FORMED_CHARACTER_CONSTANT"></span>Schlecht gebildete Zeichenkonst constant</dt> <dd> Das Zeilenendezeichen ist in Zeichenkonst constants nicht zulässig.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2109"></span><span id="midl2109"></span><dl> <dt><strong>MIDL2109</strong></dt> </dl></td>
<td><dl> <dt><span id="end_of_file_found_in_comment"></span><span id="END_OF_FILE_FOUND_IN_COMMENT"></span>Ende der Datei im Kommentar gefunden</dt> <dd> Das Dateiendezeichen wurde in einem Kommentar gefunden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2110"></span><span id="midl2110"></span><dl> <dt><strong>MIDL2110</strong></dt> </dl></td>
<td><dl> <dt><span id="end_of_file_found_in_string"></span><span id="END_OF_FILE_FOUND_IN_STRING"></span>Ende der Datei, die in der Zeichenfolge gefunden wurde</dt> <dd> Das Dateiendezeichen wurde in einer Zeichenfolge gefunden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2111"></span><span id="midl2111"></span><dl> <dt><strong>MIDL2111</strong></dt> </dl></td>
<td><dl> <dt><span id="identifier_length_exceeds_31_characters"></span><span id="IDENTIFIER_LENGTH_EXCEEDS_31_CHARACTERS"></span>Bezeichnerlänge überschreitet 31 Zeichen</dt> <dd> Bezeichner sind auf 31 alphanumerische Zeichen beschränkt. Bezeichnernamen, die länger als 31 Zeichen sind, werden abgeschnitten.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2112"></span><span id="midl2112"></span><dl> <dt><strong>MIDL2112</strong></dt> </dl></td>
<td><dl> <dt><span id="end_of_line_found_in_string"></span><span id="END_OF_LINE_FOUND_IN_STRING"></span>Ende der Zeile in der Zeichenfolge gefunden</dt> <dd> Das Zeilenendezeichen wurde in der Zeichenfolge gefunden. Stellen Sie sicher, dass Sie das doppelte Anführungszeichen eingeschlossen haben, das die Zeichenfolge beendet.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2113"></span><span id="midl2113"></span><dl> <dt><strong>MIDL2113</strong></dt> </dl></td>
<td><dl> <dt><span id="string_constant_exceeds_limit_of_255_characters"></span><span id="STRING_CONSTANT_EXCEEDS_LIMIT_OF_255_CHARACTERS"></span>Zeichenfolgenkonstkette überschreitet das Limit von 255 Zeichen</dt> <dd> Die Zeichenfolge hat die maximal zulässige Länge von 255 Zeichen überschritten.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2114"></span><span id="midl2114"></span><dl> <dt><strong>MIDL2114</strong></dt> </dl></td>
<td><dl> <dt><span id="identifier_exceeds_limit_of_255_characters_and_has_been_truncated"></span><span id="IDENTIFIER_EXCEEDS_LIMIT_OF_255_CHARACTERS_AND_HAS_BEEN_TRUNCATED"></span>Bezeichner überschreitet den Grenzwert von 255 Zeichen und wurde abgeschnitten.</dt> <dd> Der Bezeichner hat die maximal zulässige Länge von 255 Zeichen überschritten. Überflüssige Zeichen im Bezeichner werden abgeschnitten.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2115"></span><span id="midl2115"></span><dl> <dt><strong>MIDL2115</strong></dt> </dl></td>
<td><dl> <dt><span id="constant_too_big"></span><span id="CONSTANT_TOO_BIG"></span>Konstante zu groß</dt> <dd> Die Konstante ist zu groß, um intern dargestellt zu werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2116"></span><span id="midl2116"></span><dl> <dt><strong>MIDL2116</strong></dt> </dl></td>
<td><dl> <dt><span id="numerical_parsing_error"></span><span id="NUMERICAL_PARSING_ERROR"></span>Numerischer Analysefehler</dt> <dd> Der Compiler konnte den numerischen Bezeichner nicht analysieren.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2117"></span><span id="midl2117"></span><dl> <dt><strong>MIDL2117</strong></dt> </dl></td>
<td><dl> <dt><span id="error_in_opening_file"></span><span id="ERROR_IN_OPENING_FILE"></span>Fehler beim Öffnen der Datei</dt> <dd> Das Betriebssystem hat beim Versuch, eine Ausgabedatei zu öffnen, einen Fehler gemeldet. Dieser Fehler kann durch einen Namen verursacht werden, der für das Dateisystem zu lang ist, oder durch einen doppelten Dateinamen.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2118"></span><span id="midl2118"></span><dl> <dt><strong>MIDL2118</strong></dt> </dl></td>
<td>Fehlerbindung an Funktion<br/></td>
</tr>
<tr class="even">
<td><span id="MIDL2119"></span><span id="midl2119"></span><dl> <dt><strong>MIDL2119</strong></dt> </dl></td>
<td>Fehler beim Initialisieren von OLE<br/></td>
</tr>
<tr class="odd">
<td><span id="MIDL2120"></span><span id="midl2120"></span><dl> <dt><strong>MIDL2120</strong></dt> </dl></td>
<td>Fehler beim Laden der Bibliothek<br/></td>
</tr>
<tr class="even">
<td><span id="MIDL2121"></span><span id="midl2121"></span><dl> <dt><strong>MIDL2121</strong></dt> </dl></td>
<td><dl> <dt><span id="_out__only_parameter_must_not_derive_from_a_top-level__unique__or__ptr__pointer_array"></span><span id="_OUT__ONLY_PARAMETER_MUST_NOT_DERIVE_FROM_A_TOP-LEVEL__UNIQUE__OR__PTR__POINTER_ARRAY"></span>[out] Der einzige Parameter darf nicht von einem Zeiger/Array der obersten Ebene [unique] oder [ptr] ableiten.</dt> <dd> Ein eindeutiger Zeiger kann kein<a href="out-idl.md"><strong>[out</strong></a>]-only-Parameter sein. Definitionsgemäß kann ein eindeutiger Zeiger von <strong>NULL</strong> in Nicht-NULL<strong>ändern.</strong> Es werden keine Informationen über den<strong>[out</strong>]only-Parameter vom Client an den Server übergeben.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2122"></span><span id="midl2122"></span><dl> <dt><strong>MIDL2122</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_is_not_applicable_to_this_non-rpcable_union"></span><span id="ATTRIBUTE_IS_NOT_APPLICABLE_TO_THIS_NON-RPCABLE_UNION"></span>Das -Attribut gilt nicht für diese nicht rpcable-Union.</dt> <dd> Nur die Attribute [<a href="switch-is.md"><strong>switch_is</strong></a>] und [<a href="switch-type.md"><strong>switch_type</strong></a>] gelten für eine Union, die als Teil eines Remoteprozeduraufrufs übertragen wird.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2123"></span><span id="midl2123"></span><dl> <dt><strong>MIDL2123</strong></dt> </dl></td>
<td><dl> <dt><span id="expression_used_for_a_size_attribute_must_not_derive_from_an__out_-only_parameter"></span><span id="EXPRESSION_USED_FOR_A_SIZE_ATTRIBUTE_MUST_NOT_DERIVE_FROM_AN__OUT_-ONLY_PARAMETER"></span>Der für ein Größenattribut verwendete Ausdruck darf nicht von einem [out]only-Parameter ableiten.</dt> <dd> Der Wert eines<a href="out-idl.md"><strong>[out</strong></a>]-only-Parameters wird nicht an den Server übertragen und kann nicht verwendet werden, um die Länge oder Größe des Parameters [<a href="in.md"><strong>in</strong></a>] zu bestimmen.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2124"></span><span id="midl2124"></span><dl> <dt><strong>MIDL2124</strong></dt> </dl></td>
<td><dl> <dt><span id="expression_used_for_a_length_attribute_for_an__in__parameter_cannot_derive_from_an__out_-only_parameter"></span><span id="EXPRESSION_USED_FOR_A_LENGTH_ATTRIBUTE_FOR_AN__IN__PARAMETER_CANNOT_DERIVE_FROM_AN__OUT_-ONLY_PARAMETER"></span>Ausdruck, der für ein Längenattribut für einen [in]-Parameter verwendet wird, kann nicht von einem [out]only-Parameter ableiten</dt> <dd> Der Wert eines<a href="out-idl.md"><strong>[out</strong></a>]-only-Parameters wird nicht an den Server übertragen und kann nicht verwendet werden, um die Länge oder Größe des Parameters [<a href="in.md"><strong>in</strong></a>] zu bestimmen.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2125"></span><span id="midl2125"></span><dl> <dt><strong>MIDL2125</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of__int__needs__c_ext"></span><span id="USE_OF__INT__NEEDS__C_EXT"></span>Verwendung von &quot; int &quot; needs /c_ext</dt> <dd> MIDL ist eine stark typierte Sprache. Alle über das Netzwerk übertragenen Parameter müssen von einem der MIDL-Basistypen abgeleitet werden. Der Typ <a href="int.md"><strong>int</strong></a> ist nicht als Teil von MIDL definiert. Übertragene Daten müssen einen Größenbezeichner enthalten: <a href="small.md"><strong>small,</strong></a> <strong>short</strong>oder <strong>long.</strong> Daten, die nicht über das Netzwerk übertragen werden, können in eine Schnittstelle eingeschlossen werden. Verwenden Sie <a href="-c-ext.md"><strong>den Schalter /c_ext</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2126"></span><span id="midl2126"></span><dl> <dt><strong>MIDL2126</strong></dt> </dl></td>
<td><dl> <dt><span id="struct_union_field_must_not_be__void_"></span><span id="STRUCT_UNION_FIELD_MUST_NOT_BE__VOID_"></span>Das Feld "struct/union" darf nicht &quot; "void" sein.&quot;</dt> <dd> Felder in einer Struktur oder Union müssen deklariert werden, um einen bestimmten Basistyp zu haben, der von MIDL unterstützt wird, oder einen Typ, der von den Basistypen abgeleitet ist. Void-Typen sind in Remotevorgängen nicht zulässig.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2127"></span><span id="midl2127"></span><dl> <dt><strong>MIDL2127</strong></dt> </dl></td>
<td><dl> <dt><span id="array_element_must_not_be_void"></span><span id="ARRAY_ELEMENT_MUST_NOT_BE_VOID"></span>Arrayelement darf nicht void sein</dt> <dd> Ein Arrayelement kann nicht void sein.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2128"></span><span id="midl2128"></span><dl> <dt><strong>MIDL2128</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_type_qualifiers_and_or_modifiers_needs__c_ext"></span><span id="USE_OF_TYPE_QUALIFIERS_AND_OR_MODIFIERS_NEEDS__C_EXT"></span>Die Verwendung von Typqualifizierern und/oder Modifizierern benötigt /c_ext</dt> <dd> Typmodifizierer wie <strong>_cdecl</strong> und <strong>_far</strong> können nur kompiliert werden, wenn Sie den <a href="-c-ext.md"><strong>Schalter /c_ext</strong></a> angeben.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2129"></span><span id="midl2129"></span><dl> <dt><strong>MIDL2129</strong></dt> </dl></td>
<td><dl> <dt><span id="struct_union_field_must_not_derive_from_a_function"></span><span id="STRUCT_UNION_FIELD_MUST_NOT_DERIVE_FROM_A_FUNCTION"></span>Struktur/Union-Feld darf nicht von einer Funktion ableiten</dt> <dd> Die Felder einer Struktur oder Union müssen MIDL-Basistypen oder -Typen sein, die von diesen Basistypen abgeleitet werden. Funktionen sind in Struktur- oder Union-Feldern nicht zulässig.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2130"></span><span id="midl2130"></span><dl> <dt><strong>MIDL2130</strong></dt> </dl></td>
<td><dl> <dt><span id="array_element_must_not_be_a_function"></span><span id="ARRAY_ELEMENT_MUST_NOT_BE_A_FUNCTION"></span>Arrayelement darf keine Funktion sein</dt> <dd> Ein Arrayelement kann keine Funktion sein.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2131"></span><span id="midl2131"></span><dl> <dt><strong>MIDL2131</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_must_not_be_a_function"></span><span id="PARAMETER_MUST_NOT_BE_A_FUNCTION"></span>-Parameter darf keine Funktion sein</dt> <dd> Der Parameter für eine Remoteprozedur muss eine Variable eines angegebenen Typs sein. Eine Funktion kann kein Parameter für die Remoteprozedur sein.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2132"></span><span id="midl2132"></span><dl> <dt><strong>MIDL2132</strong></dt> </dl></td>
<td><dl> <dt><span id="struct_union_with_bit_fields_needs__c_ext"></span><span id="STRUCT_UNION_WITH_BIT_FIELDS_NEEDS__C_EXT"></span>struktur/union mit Bitfeldern benötigt /c_ext</dt> <dd> Sie müssen den MIDL-Compilerschalter <a href="-c-ext.md"><strong>/c_ext</strong></a> angeben, um Bitfelder in Strukturen zuzulassen, die nicht in einem Remoteprozeduraufruf übertragen werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2133"></span><span id="midl2133"></span><dl> <dt><strong>MIDL2133</strong></dt> </dl></td>
<td><dl> <dt><span id="bit_field_specification_on_a_type_other_that__int__is_a_non-ANSI-compatible_extension"></span><span id="bit_field_specification_on_a_type_other_that__int__is_a_non-ansi-compatible_extension"></span><span id="BIT_FIELD_SPECIFICATION_ON_A_TYPE_OTHER_THAT__INT__IS_A_NON-ANSI-COMPATIBLE_EXTENSION"></span>Bitfeldspezifikation für einen anderen Typ, &quot; der int &quot; eine nicht ANSI-kompatible Erweiterung ist</dt> <dd> Die ANSI C-Programmiersprachenspezifikation lässt nicht zu, dass Bitfelder auf nichtinteger-Typen angewendet werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2134"></span><span id="midl2134"></span><dl> <dt><strong>MIDL2134</strong></dt> </dl></td>
<td><dl> <dt><span id="bit_field_specification_can_be_applied_only_to_simple__integral_types"></span><span id="BIT_FIELD_SPECIFICATION_CAN_BE_APPLIED_ONLY_TO_SIMPLE__INTEGRAL_TYPES"></span>Bitfeldspezifikation kann nur auf einfache integrale Typen angewendet werden.</dt> <dd> Die ANSI C-Programmiersprachenspezifikation lässt nicht zu, dass Bitfelder auf nichtinteger-Typen angewendet werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2135"></span><span id="midl2135"></span><dl> <dt><strong>MIDL2135</strong></dt> </dl></td>
<td><dl> <dt><span id="struct_union_field_must_not_derive_from_handle_t_or_a_context-handle"></span><span id="STRUCT_UNION_FIELD_MUST_NOT_DERIVE_FROM_HANDLE_T_OR_A_CONTEXT-HANDLE"></span>Struktur-/Union-Feld darf nicht von handle_t oder einem Kontexthandle abgeleitet werden.</dt> <dd> Kontexthandles können nicht als Teil einer anderen Struktur übertragen werden. Sie müssen als Kontexthandles übertragen werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2136"></span><span id="midl2136"></span><dl> <dt><strong>MIDL2136</strong></dt> </dl></td>
<td><dl> <dt><span id="array_element_must_not_derive_from_handle_t_or_a_context_handle"></span><span id="ARRAY_ELEMENT_MUST_NOT_DERIVE_FROM_HANDLE_T_OR_A_CONTEXT_HANDLE"></span>Arrayelement darf nicht von handle_t oder einem Kontexthandle abgeleitet werden</dt> <dd> Kontexthandles können nicht als Teil eines Arrays übertragen werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2137"></span><span id="midl2137"></span><dl> <dt><strong>MIDL2137</strong></dt> </dl></td>
<td><dl> <dt><span id="this_specification_of_union_needs__c_ext"></span><span id="THIS_SPECIFICATION_OF_UNION_NEEDS__C_EXT"></span>diese Spezifikation der Unionsanforderungen /c_ext</dt> <dd> Eine Union, die in der Schnittstellendefinition angezeigt wird, muss dem diskriminanten zugeordnet oder als lokal deklariert werden. Daten, die nicht über das Netzwerk übertragen werden, können implizit als lokal deklariert werden, wenn Sie den Schalter <a href="-c-ext.md"><strong>/c_ext</strong></a> verwenden. Dies ist die MIDL-Standardeinstellung. Sie können diese IDL nicht mit dem Schalter <a href="-osf.md"><strong>/osf</strong></a> kompilieren.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2138"></span><span id="midl2138"></span><dl> <dt><strong>MIDL2138</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_deriving_from_an__int__must_have_size_specifier__small____short___or__long__with_the__int_"></span><span id="PARAMETER_DERIVING_FROM_AN__INT__MUST_HAVE_SIZE_SPECIFIER__SMALL____SHORT___OR__LONG__WITH_THE__INT_"></span>Parameter, die von einem int abgeleitet &quot; &quot; werden, müssen einen Größenspezifizierer &quot; für "small", &quot; &quot; "short" &quot; oder &quot; "long" &quot; mit dem Wert &quot; int aufweisen.&quot;</dt> <dd> Der Typ <a href="int.md"><strong>int</strong></a> ist nur ein gültiger MIDL-Typ auf 32-Bit-Plattformen, auf 16-Bit-Systemen <strong>muss int</strong> von einer Größenangabe begleitet werden. Verwenden Sie einen der Größenspezifizierer <a href="small.md"><strong>small</strong></a>, <a href="short.md"><strong>short</strong></a>oder <a href="long.md"><strong>long</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2139"></span><span id="midl2139"></span><dl> <dt><strong>MIDL2139</strong></dt> </dl></td>
<td><dl> <dt><span id="type_of_the_parameter_cannot_derive_from_void_or_void_"></span><span id="TYPE_OF_THE_PARAMETER_CANNOT_DERIVE_FROM_VOID_OR_VOID_"></span>Der Typ des Parameters kann nicht von void oder void* abgeleitet werden.</dt> <dd> MIDL ist eine stark typisierte Sprache. Alle über das Netzwerk übertragenen Parameter müssen von einem der MIDL-Basistypen abgeleitet werden. MIDL unterstützt <a href="void.md"><strong>void</strong></a> nicht als Basistyp. Sie müssen die Deklaration in einen gültigen MIDL-Typ ändern.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2140"></span><span id="midl2140"></span><dl> <dt><strong>MIDL2140</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_deriving_from_a_struct_union_containing_bit_fields_is_not_supported"></span><span id="PARAMETER_DERIVING_FROM_A_STRUCT_UNION_CONTAINING_BIT_FIELDS_IS_NOT_SUPPORTED"></span>Parameter, die von einer Struktur/Union abgeleitet werden, die Bitfelder enthält, werden nicht unterstützt.</dt> <dd> Bitfelder werden von DCE RPC nicht als gültiger Datentyp definiert.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2141"></span><span id="midl2141"></span><dl> <dt><strong>MIDL2141</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_a_parameter_deriving_from_a_type_containing_type-modifiers_type-qualifiers_needs__c_ext"></span><span id="USE_OF_A_PARAMETER_DERIVING_FROM_A_TYPE_CONTAINING_TYPE-MODIFIERS_TYPE-QUALIFIERS_NEEDS__C_EXT"></span>Die Verwendung eines Parameters, der von einem Typ abgeleitet wird, der Typmodifizierer/Typqualifizierer enthält, benötigt /c_ext</dt> <dd> Die Verwendung von Schlüsselwörtern wie <strong>far</strong>, <strong>near</strong>, <a href="const.md"><strong>const</strong></a>und <strong>volatile</strong> in der IDL-Datei ist eine Microsoft-Erweiterung für DCE RPC. Diese Schlüsselwörter sind nicht verfügbar, wenn Sie mit dem Schalter <a href="-osf.md"><strong>/osf</strong></a> kompilieren, wodurch der Standardmäßige <a href="-c-ext.md"><strong>/c_ext</strong></a> Erweiterungsschalter deaktiviert wird.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2142"></span><span id="midl2142"></span><dl> <dt><strong>MIDL2142</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_must_not_derive_from_a_pointer_to_a_function"></span><span id="PARAMETER_MUST_NOT_DERIVE_FROM_A_POINTER_TO_A_FUNCTION"></span>-Parameter darf nicht von einem Zeiger auf eine Funktion abgeleitet werden</dt> <dd> Die RPC-Laufzeitbibliotheken übertragen einen Zeiger und die zugehörigen Daten zwischen Client und Server. Zeiger auf Funktionen können nicht als Parameter übertragen werden, da die Funktion nicht über das Netzwerk übertragen werden kann.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2143"></span><span id="midl2143"></span><dl> <dt><strong>MIDL2143</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_must_not_derive_from_a_nonrpccapable_union"></span><span id="PARAMETER_MUST_NOT_DERIVE_FROM_A_NONRPCCAPABLE_UNION"></span>-Parameter darf nicht von einer Nicht-Pc-fähigen Union abgeleitet werden</dt> <dd> Die Union muss einem diskriminanten zugeordnet werden. Verwenden Sie die Attribute [<a href="switch-is.md"><strong>switch_is</strong></a>] und [<a href="switch-type.md"><strong>switch_type</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2144"></span><span id="midl2144"></span><dl> <dt><strong>MIDL2144</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_derives_from_an__int.__You_must_use_size_specifiers_with_the__int_"></span><span id="return_type_derives_from_an__int.__you_must_use_size_specifiers_with_the__int_"></span><span id="RETURN_TYPE_DERIVES_FROM_AN__INT.__YOU_MUST_USE_SIZE_SPECIFIERS_WITH_THE__INT_"></span>Der Rückgabetyp wird von einem &quot; int-Typ abgeleitet. &quot; Sie müssen Größenspezifizierer mit dem Wert int verwenden. &quot;&quot;</dt> <dd> Auf 16-Bit-Systemen ist der Typ <a href="int.md"><strong>int</strong></a> kein gültiger MIDL-Typ, es sei denn, er wird von einer Größenangabe begleitet. Verwenden Sie einen der Größenspezifizierer <a href="small.md"><strong>small</strong></a>, <a href="short.md"><strong>short</strong></a>oder <a href="long.md"><strong>long</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2145"></span><span id="midl2145"></span><dl> <dt><strong>MIDL2145</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_must_not_derive_from_a_void_pointer"></span><span id="RETURN_TYPE_MUST_NOT_DERIVE_FROM_A_VOID_POINTER"></span>Rückgabetyp darf nicht von einem void-Zeiger abgeleitet werden</dt> <dd> MIDL ist eine stark typisierte Sprache. Alle über das Netzwerk übertragenen Parameter müssen von einem der MIDL-Basistypen abgeleitet werden. Void-Typen sind nicht als Teil von MIDL definiert. Sie müssen die Deklaration in einen gültigen MIDL-Typ ändern.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2146"></span><span id="midl2146"></span><dl> <dt><strong>MIDL2146</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_must_not_derive_from_a_structure_union_containing_bit-fields"></span><span id="RETURN_TYPE_MUST_NOT_DERIVE_FROM_A_STRUCTURE_UNION_CONTAINING_BIT-FIELDS"></span>Der Rückgabetyp darf nicht von einer Struktur/Union abgeleitet werden, die Bitfelder enthält.</dt> <dd> Bitfelder werden von DCE RPC nicht als gültiger Datentyp definiert.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2147"></span><span id="midl2147"></span><dl> <dt><strong>MIDL2147</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_must_not_derive_from_a_nonrpccapable_union"></span><span id="RETURN_TYPE_MUST_NOT_DERIVE_FROM_A_NONRPCCAPABLE_UNION"></span>Der Rückgabetyp darf nicht von einer Nicht-Pc-fähigen Union abgeleitet werden.</dt> <dd> Die Union muss einem diskriminanten zugeordnet werden. Verwenden Sie die Attribute [<a href="switch-is.md"><strong>switch_is</strong></a>] und [<a href="switch-type.md"><strong>switch_type</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2148"></span><span id="midl2148"></span><dl> <dt><strong>MIDL2148</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_must_not_derive_from_a_pointer_to_a_function"></span><span id="RETURN_TYPE_MUST_NOT_DERIVE_FROM_A_POINTER_TO_A_FUNCTION"></span>Rückgabetyp darf nicht von einem Zeiger auf eine Funktion abgeleitet werden</dt> <dd> Die RPC-Laufzeitbibliotheken übertragen einen Zeiger und die zugehörigen Daten zwischen Client und Server. Zeiger auf Funktionen können nicht als Parameter übertragen werden, da RPC keine Methode zum Übertragen der zugeordneten Funktion über das Netzwerk definiert.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2149"></span><span id="midl2149"></span><dl> <dt><strong>MIDL2149</strong></dt> </dl></td>
<td><dl> <dt><span id="compound_initializers_are_not_supported"></span><span id="COMPOUND_INITIALIZERS_ARE_NOT_SUPPORTED"></span>Zusammengesetzte Initialisierer werden nicht unterstützt.</dt> <dd> DCE RPC unterstützt nur die einfache Initialisierung. Die Struktur oder das Array kann nicht in der IDL-Datei initialisiert werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2150"></span><span id="midl2150"></span><dl> <dt><strong>MIDL2150</strong></dt> </dl></td>
<td><dl> <dt><span id="ACF_attributes_in_the_IDL_file_need_the__app_config_switch"></span><span id="acf_attributes_in_the_idl_file_need_the__app_config_switch"></span><span id="ACF_ATTRIBUTES_IN_THE_IDL_FILE_NEED_THE__APP_CONFIG_SWITCH"></span>ACF-Attribute in der IDL-Datei benötigen den Schalter /app_config</dt> <dd> Mit einer Microsoft-Erweiterung können Sie ACF-Attribute in der IDL-Datei angeben. Verwenden Sie den Schalter <a href="-app-config.md"><strong>/app_config,</strong></a> um diese Erweiterung zu aktivieren.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2151"></span><span id="midl2151"></span><dl> <dt><strong>MIDL2151</strong></dt> </dl></td>
<td><dl> <dt><span id="single-line_comment_needs__ms_ext_or__c_ext"></span><span id="SINGLE-LINE_COMMENT_NEEDS__MS_EXT_OR__C_EXT"></span>Einzeilige Kommentare benötigen /ms_ext oder /c_ext</dt> <dd> Einzeilige Kommentare, die zwei Schrägstriche (/) verwenden, stellen eine Microsoft-Erweiterung für DCE RPC dar. Sie können keine einzeiligen Kommentare verwenden, wenn Sie mit dem Schalter <a href="-osf.md"><strong>/osf</strong></a> kompilieren.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2152"></span><span id="midl2152"></span><dl> <dt><strong>MIDL2152</strong></dt> </dl></td>
<td><dl> <dt><span id="_version__format_is_incorrect"></span><span id="_VERSION__FORMAT_IS_INCORRECT"></span>[Version] Format ist falsch</dt> <dd> Die Versionsnummer der Schnittstelle im Schnittstellenheader muss im Format <em>Hauptversion</em>angegeben werden. <em>Nebenversion,</em>wobei jede Zahl zwischen 0 und 65535 liegen kann.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2153"></span><span id="midl2153"></span><dl> <dt><strong>MIDL2153</strong></dt> </dl></td>
<td><dl> <dt><span id="_signed__needs__ms_ext_or__c_ext"></span><span id="_SIGNED__NEEDS__MS_EXT_OR__C_EXT"></span>&quot;signed &quot; benötigt /ms_ext oder /c_ext</dt> <dd> Die Verwendung des <a href="signed.md"><strong>Schlüsselworts signed</strong></a> ist eine Microsoft-Erweiterung für DCE RPC. Sie können den Schalter <a href="-osf.md"><strong>/osf</strong></a> nicht verwenden, wenn Sie dieses Feature verwenden möchten.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2154"></span><span id="midl2154"></span><dl> <dt><strong>MIDL2154</strong></dt> </dl></td>
<td><dl> <dt><span id="mismatch_in_assignment_type"></span><span id="MISMATCH_IN_ASSIGNMENT_TYPE"></span>Konflikt beim Zuweisungstyp</dt> <dd> Der Typ der Variablen stimmt nicht mit dem Typ des Werts überein, der der Variablen zugewiesen ist.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2155"></span><span id="midl2155"></span><dl> <dt><strong>MIDL2155</strong></dt> </dl></td>
<td><dl> <dt><span id="declaration_must_be_of_the_form__const__type__declarator_____initializing_expression_"></span><span id="DECLARATION_MUST_BE_OF_THE_FORM__CONST__TYPE__DECLARATOR_____INITIALIZING_EXPRESSION_"></span>-Deklaration muss folgendes Format &lt; aufweisen: const-Typ&gt;<declarator> = <initializing expression></dt> <dd> Die Deklaration ist nicht mit der DCE-RPC-Syntax kompatibel. Verwenden Sie <a href="-ms-ext.md"><strong>den Compilermodusschalter /ms_ext</strong></a> <a href="-c-ext.md"><strong>oder /c_ext</strong></a> MIDL.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2156"></span><span id="midl2156"></span><dl> <dt><strong>MIDL2156</strong></dt> </dl></td>
<td><dl> <dt><span id="declaration_must_have__const_"></span><span id="DECLARATION_MUST_HAVE__CONST_"></span>Deklaration muss const &quot; haben&quot;</dt> <dd> Deklarationen in der IDL-Datei müssen konstante Ausdrücke sein, die das Schlüsselwort <a href="const.md"><strong>const</strong></a>verwenden. Beispiel:<br/>
<pre class="syntax" data-space="preserve"><code>const short x = 2;</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2157"></span><span id="midl2157"></span><dl> <dt><strong>MIDL2157</strong></dt> </dl></td>
<td><dl> <dt><span id="struct_union_enum_must_not_be_defined_in_a_parameter-type_specification"></span><span id="STRUCT_UNION_ENUM_MUST_NOT_BE_DEFINED_IN_A_PARAMETER-TYPE_SPECIFICATION"></span>struct/union/enum darf nicht in einer Parametertypspezifikation definiert werden</dt> <dd> Der struktur-, union- oder enumerierte Typ muss außerhalb des Funktionsprototyps explizit angegeben werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2158"></span><span id="midl2158"></span><dl> <dt><strong>MIDL2158</strong></dt> </dl></td>
<td><dl> <dt><span id="_allocate__attribute_must_be_applied_only_on_non-void_pointer_types"></span><span id="_ALLOCATE__ATTRIBUTE_MUST_BE_APPLIED_ONLY_ON_NON-VOID_POINTER_TYPES"></span>Das Attribut [allocate] darf nur auf Zeigertypen angewendet werden, die nicht void sind.</dt> <dd> Das Attribut [<a href="allocate.md"><strong>allocate</strong></a>] ist für komplexe zeigerbasierte Datenstrukturen konzipiert. Wenn das Attribut [allocate] angegeben wird, durchläuft die Stubdatei die Datenstruktur, um die Gesamtgröße aller Objekte zu berechnen, auf die über den Zeiger und alle anderen Zeiger in der Datenstruktur zugegriffen werden kann. Ändern Sie den Typ in einen zeigerfreien Typ, oder entfernen Sie das Attribut [<strong>allocate</strong>], und verwenden Sie eine andere Methode, um die Zuordnungsgröße zu bestimmen, z. B. <strong>den sizeof-Operator.</strong><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2159"></span><span id="midl2159"></span><dl> <dt><strong>MIDL2159</strong></dt> </dl></td>
<td><dl> <dt><span id="array_or_equivalent_pointer_construct_cannot_derive_from_a_nonencapsulated_union"></span><span id="ARRAY_OR_EQUIVALENT_POINTER_CONSTRUCT_CANNOT_DERIVE_FROM_A_NONENCAPSULATED_UNION"></span>Array- oder äquivalentes Zeigerkonstrukt kann nicht von einer nicht kapselten Union ableiten</dt> <dd> Jede Union muss einem diskriminanten zugeordnet werden. Arrays von Unions sind nicht zulässig, da sie die zugeordnete Diskriminanz nicht bereitstellen. Arrays von -Strukturen, in denen die -Struktur die Union und ihre Diskriminanz verpackt, sind zulässig, da die Stubs die Diskriminanz verwenden können, um die Größe der einzelnen Unions zu bestimmen.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2160"></span><span id="midl2160"></span><dl> <dt><strong>MIDL2160</strong></dt> </dl></td>
<td><dl> <dt><span id="field_must_not_derive_from_an_error_status_t_type"></span><span id="FIELD_MUST_NOT_DERIVE_FROM_AN_ERROR_STATUS_T_TYPE"></span>Feld darf nicht von einem error_status_t ableiten</dt> <dd> Der <a href="error-status-t.md"><strong>error_status_t</strong></a> kann nur als Parameter oder Rückgabetyp verwendet werden. Sie kann nicht in das Feld einer Struktur oder Union eingebettet werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2161"></span><span id="midl2161"></span><dl> <dt><strong>MIDL2161</strong></dt> </dl></td>
<td><dl> <dt><span id="union_has_at_least_one_arm_without_a_case_label"></span><span id="UNION_HAS_AT_LEAST_ONE_ARM_WITHOUT_A_CASE_LABEL"></span>union verfügt über mindestens einen Arm ohne Case-Bezeichnung</dt> <dd> Die Union-Deklaration passt nicht zur erforderlichen MIDL-Syntax für die Union. Jeder Union-Arm erfordert eine Case-Bezeichnung oder Standardbezeichnung, die diesen Union-Arm auswählt.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2162"></span><span id="midl2162"></span><dl> <dt><strong>MIDL2162</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_or_return_value_must_not_derive_from_a_type_that_has__ignore__applied_to_it"></span><span id="PARAMETER_OR_RETURN_VALUE_MUST_NOT_DERIVE_FROM_A_TYPE_THAT_HAS__IGNORE__APPLIED_TO_IT"></span>Parameter oder Rückgabewert darf nicht von einem Typ ableiten, auf den [ignore] angewendet wurde.</dt> <dd> Das Attribut [<a href="ignore.md"><strong>ignore</strong></a>] ist ein Feldattribut, das nur auf Felder angewendet werden kann, z. B. Felder von Strukturen und Arrays. Das [<strong>ignore</strong>] -Attribut gibt an, dass der Stub den Zeiger während der Übertragung nicht dereferenzieren soll und nicht zulässig ist, wenn er konflikte mit anderen Attributen, die dereferenziert werden müssen, z. B. [<a href="out-idl.md"><strong>out</strong></a>] -Parameter und Funktionsrück rückgabewerte.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2163"></span><span id="midl2163"></span><dl> <dt><strong>MIDL2163</strong></dt> </dl></td>
<td><dl> <dt><span id="pointer_already_has_a_pointer_attribute_applied_to_it"></span><span id="POINTER_ALREADY_HAS_A_POINTER_ATTRIBUTE_APPLIED_TO_IT"></span>Auf den Zeiger wurde bereits ein Zeigerattribut angewendet.</dt> <dd> Nur eines der Zeigerattribute [<a href="ref.md"><strong>ref</strong></a>], [<a href="unique.md"><strong>unique</strong></a>], oder [<a href="ptr.md"><strong>ptr</strong></a>] kann auf einen einzelnen Zeiger angewendet werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2164"></span><span id="midl2164"></span><dl> <dt><strong>MIDL2164</strong></dt> </dl></td>
<td><dl> <dt><span id="field_parameter_must_not_derive_from_a_structure_that_is_recursive_through_a_ref_pointer"></span><span id="FIELD_PARAMETER_MUST_NOT_DERIVE_FROM_A_STRUCTURE_THAT_IS_RECURSIVE_THROUGH_A_REF_POINTER"></span>Field/Parameter darf nicht von einer Struktur ableiten, die über einen Verweiszeiger rekursiv ist.</dt> <dd> Definitionsgemäß kann ein Verweiszeiger nicht auf NULL <strong>festgelegt werden.</strong> Eine rekursive Datenstruktur, die mit einem Verweiszeiger definiert ist, verfügt über keine <strong>NULL-Elemente</strong> und ist standardmäßig nicht determinierend. Verwenden Sie ein [<a href="unique.md"><strong>unique</strong></a>] -Zeigerattribut, damit die Datenstruktur ein <strong>NULL-Element</strong> angeben kann, oder definieren Sie die Datenstruktur als nicht rekursive Datenstruktur neu.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2165"></span><span id="midl2165"></span><dl> <dt><strong>MIDL2165</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_field_deriving_from_a_void_pointer_needs__c_ext"></span><span id="USE_OF_FIELD_DERIVING_FROM_A_VOID_POINTER_NEEDS__C_EXT"></span>Die Verwendung eines Felds, das von einem void-Zeiger ableitung, benötigt /c_ext</dt> <dd> Der Typ <strong>void *</strong> und andere Typen und Typqualifizierer, die von DCE IDL nicht unterstützt werden, sind in der IDL-Datei nur zulässig, wenn Sie die MIDL-Standardcompilereinstellungen verwenden. Durch die Verwendung <a href="-osf.md"><strong>des Schalters /osf</strong></a> wird dieser Standardwert überschrieben. Wenn Sie im Osf-Kompatibilitätsmodus kompilieren müssen, müssen Sie den Zeigertyp neu definieren.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2166"></span><span id="midl2166"></span><dl> <dt><strong>MIDL2166</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_this_attribute_needs__ms_ext"></span><span id="USE_OF_THIS_ATTRIBUTE_NEEDS__MS_EXT"></span>Die Verwendung dieses Attributs benötigt /ms_ext</dt> <dd> Dieses Sprachfeature ist eine Microsoft-Erweiterung für DCE-IDL. Sie können dieses Feature nicht verwenden, wenn Sie im Osf-Kompatibilitätsmodus kompilieren ( <a href="-osf.md"><strong>/osf</strong></a> ).<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2167"></span><span id="midl2167"></span><dl> <dt><strong>MIDL2167</strong></dt> </dl></td>
<td><dl> <dt><span id="this_attribute_only_allowed_with_new_format_type_libraries"></span><span id="THIS_ATTRIBUTE_ONLY_ALLOWED_WITH_NEW_FORMAT_TYPE_LIBRARIES"></span>Dieses Attribut ist nur mit neuen Formattypbibliotheken zulässig.</dt> <dd> Um dieses Attribut verwenden zu können, benötigen Sie die version of Oleaut32.dll, die mit Windows 2000 oder höher bereitgestellt wird.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2168"></span><span id="midl2168"></span><dl> <dt><strong>MIDL2168</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_wchar_t_needs__ms_ext_or__c_ext"></span><span id="USE_OF_WCHAR_T_NEEDS__MS_EXT_OR__C_EXT"></span>Die Verwendung wchar_t benötigt /ms_ext oder /c_ext</dt> <dd> Der Breitzeichentyp stellt eine Erweiterung der DCE-IDL dar. Der MIDL-Compiler akzeptiert den Breitzeichentyp nicht, wenn Sie den <a href="-osf.md"><strong>Schalter /osf</strong></a> angeben.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2169"></span><span id="midl2169"></span><dl> <dt><strong>MIDL2169</strong></dt> </dl></td>
<td><dl> <dt><span id="unnamed_fields_need__ms_ext_or__c_ext"></span><span id="UNNAMED_FIELDS_NEED__MS_EXT_OR__C_EXT"></span>Unbenannte Felder benötigen /ms_ext oder /c_ext</dt> <dd> DCE-IDL unterstützt nicht die Verwendung unbenannten Strukturen oder Unions, die in andere Strukturen oder Unions eingebettet sind. In DER DCE-IDL müssen alle eingebetteten Felder benannt werden. Der MIDL-Compiler lässt seine Verwendung nicht zu, wenn Sie den <a href="-osf.md"><strong>Schalter /osf</strong></a> angeben.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2170"></span><span id="midl2170"></span><dl> <dt><strong>MIDL2170</strong></dt> </dl></td>
<td><dl> <dt><span id="unnamed_fields_can_derive_only_from_struct_union_types"></span><span id="UNNAMED_FIELDS_CAN_DERIVE_ONLY_FROM_STRUCT_UNION_TYPES"></span>Unbenannte Felder können nur von Struktur-/Union-Typen ableiten.</dt> <dd> Die Microsoft-Erweiterung für die DCE-IDL, die unbenannte Felder unterstützt, gilt nur für Strukturen und Unions. Sie müssen dem Feld einen Namen zuweisen oder das Feld neu definieren, um dieser Einschränkung zu entsprechen.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2171"></span><span id="midl2171"></span><dl> <dt><strong>MIDL2171</strong></dt> </dl></td>
<td><dl> <dt><span id="field_of_a_union_cannot_derive_from_a_conformant_varying_array_or_its_pointer_equivalent"></span><span id="FIELD_OF_A_UNION_CANNOT_DERIVE_FROM_A_CONFORMANT_VARYING_ARRAY_OR_ITS_POINTER_EQUIVALENT"></span>Das Feld einer Union kann nicht von einem konformen/variierenden Array oder dessen Zeigerentsprechung ableiten.</dt> <dd> Das konforme Array kann nicht allein in der Union angezeigt werden, sondern muss von dem Wert begleitet werden, der die Größe des Arrays angibt. Anstatt das Array als Union-Arm zu verwenden, verwenden Sie eine -Struktur, die aus dem konformen Array und dem Bezeichner besteht, der seine Größe angibt.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2172"></span><span id="midl2172"></span><dl> <dt><strong>MIDL2172</strong></dt> </dl></td>
<td><dl> <dt><span id="no__pointer_default__attribute_specified__assuming__ptr__for_all_unattributed_pointers_in_interface"></span><span id="NO__POINTER_DEFAULT__ATTRIBUTE_SPECIFIED__ASSUMING__PTR__FOR_ALL_UNATTRIBUTED_POINTERS_IN_INTERFACE"></span>kein [pointer_default]-Attribut angegeben, vorausgesetzt[ptr] für alle nicht attributierten Zeiger in der Schnittstelle</dt> <dd> Die DCE-IDL-Implementierung gibt an, dass alle Zeiger in jeder IDL-Datei Zeigerattributen zugeordnet werden müssen. Wenn dem Parameter- oder Zeigertyp kein explizites Zeigerattribut zugewiesen ist und kein [<a href="pointer-default.md"><strong>pointer_default</strong></a>] -Attribut in der IDL-Datei angegeben ist, wird dem Zeiger das vollständige Zeigerattribut <a href="ptr.md"><strong>ptr</strong></a> zugeordnet. Sie können die Zeigerattribute ändern, indem Sie explizite Zeigerattribute verwenden, indem Sie ein<strong>[pointer_default</strong>]-Attribut angeben oder indem Sie den <a href="-ms-ext.md"><strong>Schalter /ms_ext</strong></a> angeben, um den Standardwert für nicht attributierte Zeiger in [<a href="unique.md"><strong>unique</strong></a>] zu ändern.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2173"></span><span id="midl2173"></span><dl> <dt><strong>MIDL2173</strong></dt> </dl></td>
<td><dl> <dt><span id="initializing_expression_must_resolve_to_a_constant_expression"></span><span id="INITIALIZING_EXPRESSION_MUST_RESOLVE_TO_A_CONSTANT_EXPRESSION"></span>Initialisieren des Ausdrucks muss in einen konstanten Ausdruck auflösen</dt> <dd> Wenn ein Ausdruck als Initialisierer verwendet wird, muss der Ausdruck ein konstanter Ausdruck sein. Dies gilt für alle MIDL-Compilermodi. Der Ausdruck muss zur Kompilierzeit auflösbar sein. Geben Sie eine literale Konstante oder einen Ausdruck an, der in eine Konstante und nicht in eine Variable auflöset.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2174"></span><span id="midl2174"></span><dl> <dt><strong>MIDL2174</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_expression_must_be_of_type_integer__char__Boolean_or_enum"></span><span id="attribute_expression_must_be_of_type_integer__char__boolean_or_enum"></span><span id="ATTRIBUTE_EXPRESSION_MUST_BE_OF_TYPE_INTEGER__CHAR__BOOLEAN_OR_ENUM"></span>Attributausdruck muss vom Typ integer, char, boolean oder enum sein.</dt> <dd> Der angegebene Typ wird nicht in einen gültigen Switchtyp auflösen. Verwenden Sie einen integer-, character-, <a href="byte.md"><strong>byte-,</strong></a> <a href="boolean.md"><strong>boolean-</strong></a>oder <a href="enum.md"><strong>enum-Typ</strong></a> oder einen Typ, der von einem dieser Typen abgeleitet ist.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2175"></span><span id="midl2175"></span><dl> <dt><strong>MIDL2175</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_constant"></span><span id="ILLEGAL_CONSTANT"></span>Ungültige Konstante</dt> <dd> Die angegebene Konstante liegt nicht im gültigen Bereich für den angegebenen Typ.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2176"></span><span id="midl2176"></span><dl> <dt><strong>MIDL2176</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_not_implemented__ignored"></span><span id="ATTRIBUTE_NOT_IMPLEMENTED__IGNORED"></span>-Attribut nicht implementiert; Ignoriert</dt> <dd> Das angegebene Attribut ist in dieser Version von Microsoft RPC nicht implementiert. Der MIDL-Compiler setzt die Verarbeitung der IDL-Datei so fort, als ob das Attribut nicht vorhanden wäre.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2177"></span><span id="midl2177"></span><dl> <dt><strong>MIDL2177</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_must_not_derive_from_a__ref__pointer"></span><span id="RETURN_TYPE_MUST_NOT_DERIVE_FROM_A__REF__POINTER"></span>Der Rückgabetyp darf nicht von einem [ref]-Zeiger ableiten.</dt> <dd> Funktions-Rückgabewerte, die als Zeigertypen definiert sind, müssen als [<a href="unique.md"><strong>unique</strong></a>] oder <a href="ptr.md"><strong>vollständige Zeiger angegeben</strong></a> werden. Verweisze0er können nicht verwendet werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2178"></span><span id="midl2178"></span><dl> <dt><strong>MIDL2178</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_expression_must_be_a_variable_name_or_a_pointer_dereference_expression_in_this_mode._You_must_specify_the__ms_ext_switch"></span><span id="attribute_expression_must_be_a_variable_name_or_a_pointer_dereference_expression_in_this_mode._you_must_specify_the__ms_ext_switch"></span><span id="ATTRIBUTE_EXPRESSION_MUST_BE_A_VARIABLE_NAME_OR_A_POINTER_DEREFERENCE_EXPRESSION_IN_THIS_MODE._YOU_MUST_SPECIFY_THE__MS_EXT_SWITCH"></span>Attributausdruck muss in diesem Modus ein Variablenname oder ein Zeigerdereferenzierungsausdruck sein. Sie müssen den Schalter /ms_ext angeben.</dt> <dd> Der DCE-IDL-Compiler erfordert, dass die größe, die dem<a href="size-is.md"><strong>[size_is</strong></a>]-Attribut zugeordnet ist, durch eine Variable oder Zeigervariable angegeben wird. Wenn Sie die Microsoft-Erweiterung nutzen möchten, die die Definition des Attributs<strong>[size_is</strong>] durch einen konstanten Ausdruck zulässt, können Sie den <a href="-osf.md"><strong>Compilerschalter /osf nicht</strong></a> verwenden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2179"></span><span id="midl2179"></span><dl> <dt><strong>MIDL2179</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_must_not_derive_from_a_recursive_nonencapsulated_union"></span><span id="PARAMETER_MUST_NOT_DERIVE_FROM_A_RECURSIVE_NONENCAPSULATED_UNION"></span>Parameter darf nicht von einer rekursiven nicht kapselten Union ableiten</dt> <dd> Eine Union muss eine diskriminante enthalten, sodass eine Union keine andere Union als Element haben kann. Eine Union kann nur dann in eine andere Union eingebettet werden, wenn sie Teil einer Struktur ist, die den diskriminanten enthält.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2180"></span><span id="midl2180"></span><dl> <dt><strong>MIDL2180</strong></dt> </dl></td>
<td><dl> <dt><span id="binding-handle_parameter_cannot_be__out__only"></span><span id="BINDING-HANDLE_PARAMETER_CANNOT_BE__OUT__ONLY"></span>Der Bindungshandleparameter darf nicht nur [out] sein.</dt> <dd> Der vom MIDL-Compiler als Bindungshandle für diesen Vorgang identifizierte Handleparameter muss ein<a href="in.md"><strong>[in</strong></a>]-Parameter sein. [out]-only-Parameter sind für den Clientstub nicht definiert, und das Bindungshandle muss auf dem Client definiert werden.<a href="out-idl.md"><strong></strong></a><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2181"></span><span id="midl2181"></span><dl> <dt><strong>MIDL2181</strong></dt> </dl></td>
<td><dl> <dt><span id="pointer_to_a_handle_cannot_be__unique__or__ptr_"></span><span id="POINTER_TO_A_HANDLE_CANNOT_BE__UNIQUE__OR__PTR_"></span>Zeiger auf ein Handle darf nicht [eindeutig] oder [ptr] sein.</dt> <dd> Sie können die eindeutigen und vollständigen Zeigerattribute nicht für einen Zeiger auf ein Handle verwenden. Diese Attribute lassen den Wert <strong>NULL</strong>zu, und das Bindungshandle darf nicht <strong>NULL</strong>sein. Verwenden Sie das<a href="ref.md"><strong>[ref</strong></a>]-Attribut, um den Bindungshandleparameter von Verweiszeigern abzuleiten.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2182"></span><span id="midl2182"></span><dl> <dt><strong>MIDL2182</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_that_is_not_a_binding_handle_must_not_derive_from_handle_t"></span><span id="PARAMETER_THAT_IS_NOT_A_BINDING_HANDLE_MUST_NOT_DERIVE_FROM_HANDLE_T"></span>-Parameter, der kein Bindungshandle ist, darf nicht von handle_t</dt> <dd> Der primitive Handletyp <a href="handle-t.md"><strong>handle_t</strong></a> ist kein gültiger Datentyp, der über das Netzwerk übertragen wird. Ändern Sie den Parametertyp in einen anderen Typ als <strong>handle_t</strong>, oder entfernen Sie den Parameter.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2183"></span><span id="midl2183"></span><dl> <dt><strong>MIDL2183</strong></dt> </dl></td>
<td><dl> <dt><span id="unexpected_end_of_file_found"></span><span id="UNEXPECTED_END_OF_FILE_FOUND"></span>Unerwartetes Dateiende gefunden</dt> <dd> Der MIDL-Compiler hat das Ende der Datei gefunden, bevor er alle syntaktischen Elemente der Datei erfolgreich auflösen konnte. Vergewissern Sie sich, dass das abschließende zeichen mit der rechten Klammer (}) am Ende der Datei vorhanden ist, oder überprüfen Sie die Syntax.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2184"></span><span id="midl2184"></span><dl> <dt><strong>MIDL2184</strong></dt> </dl></td>
<td><dl> <dt><span id="type_deriving_from_handle_t_must_not_have__transmit_as__applied_to_it"></span><span id="TYPE_DERIVING_FROM_HANDLE_T_MUST_NOT_HAVE__TRANSMIT_AS__APPLIED_TO_IT"></span>Auf den Typ, der von handle_t abgeleitet wird, darf [transmit_as] nicht angewendet werden.</dt> <dd> Der primitive Handletyp <a href="handle-t.md"><strong>handle_t</strong></a> wird nicht über das Netzwerk übertragen.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2185"></span><span id="midl2185"></span><dl> <dt><strong>MIDL2185</strong></dt> </dl></td>
<td><dl> <dt><span id="_context_handle__must_not_be_applied_to_a_type_that_has__handle__applied_to_it"></span><span id="_CONTEXT_HANDLE__MUST_NOT_BE_APPLIED_TO_A_TYPE_THAT_HAS__HANDLE__APPLIED_TO_IT"></span>[context_handle] darf nicht auf einen Typ angewendet werden, auf den [handle] angewendet wurde.</dt> <dd> Die Attribute [<a href="context-handle.md"><strong>context_handle</strong></a>] und [<a href="handle.md"><strong>handle</strong></a>] können nicht auf denselben Typ angewendet werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2186"></span><span id="midl2186"></span><dl> <dt><strong>MIDL2186</strong></dt> </dl></td>
<td><dl> <dt><span id="_handle__must_not_be_specified_on_a_type_deriving_from_void_or_void__"></span><span id="_HANDLE__MUST_NOT_BE_SPECIFIED_ON_A_TYPE_DERIVING_FROM_VOID_OR_VOID__"></span>[handle] darf nicht für einen Typ angegeben werden, der von void oder void * abgeleitet wird.</dt> <dd> Ein mit dem<a href="handle.md"><strong>[handle]-Attribut</strong></a>angegebener Typ kann über das Netzwerk übertragen werden, aber der Typ <strong>void*</strong> ist kein transstrukter Typ. Der Handletyp muss in einen Typ aufgelöst werden, der von den transzenden Basistypen abgeleitet wird.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2187"></span><span id="midl2187"></span><dl> <dt><strong>MIDL2187</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_must_have_either__in____out__or__in_out__in_this_mode._You_must_specify__ms_ext_or__c_ext"></span><span id="parameter_must_have_either__in____out__or__in_out__in_this_mode._you_must_specify__ms_ext_or__c_ext"></span><span id="PARAMETER_MUST_HAVE_EITHER__IN____OUT__OR__IN_OUT__IN_THIS_MODE._YOU_MUST_SPECIFY__MS_EXT_OR__C_EXT"></span>-Parameter müssen in diesem Modus entweder [in], [out] oder [in,out] aufweisen. Sie müssen /ms_ext oder /c_ext angeben.</dt> <dd> Der DCE-IDL-Compiler erfordert, dass alle Parameter über explizite direktionale Parameter verfügen. Um die Microsoft-Erweiterungen für DCE IDL zu verwenden, können Sie den Schalter <a href="-osf.md"><strong>/osf</strong></a> nicht verwenden, der <a href="-ms-ext.md"><strong>/ms_ext</strong></a> und <a href="-c-ext.md"><strong>/c_ext</strong></a>überschreibt.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2188"></span><span id="midl2188"></span><dl> <dt><strong>MIDL2188</strong></dt> </dl></td>
<td><dl> <dt><span id="transmitted_type_may_not_derive_from__void__for__transmit_as____represent_as____wire_marshal____user_marshal_"></span><span id="TRANSMITTED_TYPE_MAY_NOT_DERIVE_FROM__VOID__FOR__TRANSMIT_AS____REPRESENT_AS____WIRE_MARSHAL____USER_MARSHAL_"></span>Der übertragene Typ kann &quot; &quot; für [transmit_as], [represent_as], [wire_marshal], [user_marshal] nicht von void abgeleitet werden.</dt> <dd> Das Attribut [<a href="transmit-as.md"><strong>transmit_as</strong></a>] gilt nur für Zeigertypen. Verwenden Sie anstelle von <a href="void.md"><strong>void</strong></a>den Typ <strong>void*.</strong><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2189"></span><span id="midl2189"></span><dl> <dt><strong>MIDL2189</strong></dt> </dl></td>
<td><dl> <dt><span id="_void__must_be_specified_on_the_first_and_only_parameter_specification"></span><span id="_VOID__MUST_BE_SPECIFIED_ON_THE_FIRST_AND_ONLY_PARAMETER_SPECIFICATION"></span>&quot;void &quot; muss in der ersten und einzigen Parameterspezifikation angegeben werden.</dt> <dd> Das Schlüsselwort <a href="void.md"><strong>void</strong></a> wird fälschlicherweise mit anderen Funktionsparametern angezeigt. Um eine Funktion ohne Parameter anzugeben, muss das Schlüsselwort <strong>void</strong> das einzige Element der Parameterliste sein, wie im folgenden Beispiel:<br/>
<pre class="syntax" data-space="preserve"><code>void Moo(void)</code></pre>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2190"></span><span id="midl2190"></span><dl> <dt><strong>MIDL2190</strong></dt> </dl></td>
<td><dl> <dt><span id="_switch_is__must_be_specified_only_on_a_type_deriving_from_a_nonencapsulated_union"></span><span id="_SWITCH_IS__MUST_BE_SPECIFIED_ONLY_ON_A_TYPE_DERIVING_FROM_A_NONENCAPSULATED_UNION"></span>[switch_is] darf nur für einen Typ angegeben werden, der von einer nicht gekapselten Union abgeleitet wird.</dt> <dd> Das Schlüsselwort [<a href="switch-is.md"><strong>switch_is</strong></a>] wird falsch angewendet. Sie kann nur mit <a href="nonencapsulated-unions.md">nicht gekapselten Union-Typen</a>verwendet werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2191"></span><span id="midl2191"></span><dl> <dt><strong>MIDL2191</strong></dt> </dl></td>
<td><dl> <dt><span id="stringable_structures_are_not_implemented_in_this_version"></span><span id="STRINGABLE_STRUCTURES_ARE_NOT_IMPLEMENTED_IN_THIS_VERSION"></span>Zeichenfolgenstrukturen sind in dieser Version nicht implementiert.</dt> <dd> DCE-IDL ermöglicht dem Attribut [<a href="string.md"><strong>String</strong></a>] das Anwenden auf eine Struktur, deren Elemente nur aus Zeichen, Bytes oder Typen bestehen, die in Zeichen oder Bytes aufgelöst werden. Diese Funktionalität wird in Microsoft RPC nicht unterstützt. Das Attribut [<strong>string</strong>] kann nicht auf die struktur als Ganzes angewendet werden. Sie kann jedoch auf jedes einzelne Array angewendet werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2192"></span><span id="midl2192"></span><dl> <dt><strong>MIDL2192</strong></dt> </dl></td>
<td><dl> <dt><span id="switch_type_can_only_be_integral__char__Boolean_or_enum"></span><span id="switch_type_can_only_be_integral__char__boolean_or_enum"></span><span id="SWITCH_TYPE_CAN_ONLY_BE_INTEGRAL__CHAR__BOOLEAN_OR_ENUM"></span>switch type kann nur integral, char, boolean oder enum sein.</dt> <dd> Der angegebene Typ wird nicht in einen gültigen Switchtyp aufgelöst. Verwenden Sie eine ganze Zahl, ein Zeichen, <a href="byte.md"><strong>ein Byte,</strong></a>einen <a href="boolean.md"><strong>booleschen</strong></a>, <a href="enum.md"><strong>einen Enumerationstyp</strong></a> oder einen Typ, der von einem dieser Typen abgeleitet ist.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2193"></span><span id="midl2193"></span><dl> <dt><strong>MIDL2193</strong></dt> </dl></td>
<td><dl> <dt><span id="_handle__must_not_be_specified_on_a_type_deriving_from_handle_t"></span><span id="_HANDLE__MUST_NOT_BE_SPECIFIED_ON_A_TYPE_DERIVING_FROM_HANDLE_T"></span>[handle] darf nicht für einen Typ angegeben werden, der von handle_t</dt> <dd> Ein Handletyp muss mit einem und nur einem der Handletypen oder Attribute definiert werden. Verwenden Sie den primitiven Typ <a href="handle-t.md"><strong>handle_t</strong></a> oder das Attribut [<a href="handle.md"><strong>handle</strong></a>], aber nicht beides. Der benutzerdefinierte Handletyp muss transkadiert sein, aber der <strong>handle_t</strong> Typ wird nicht im Netzwerk übertragen.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2194"></span><span id="midl2194"></span><dl> <dt><strong>MIDL2194</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_deriving_from_handle_t_must_not_be_an__out__parameter"></span><span id="PARAMETER_DERIVING_FROM_HANDLE_T_MUST_NOT_BE_AN__OUT__PARAMETER"></span>Parameter, der von handle_t abgeleitet wird, darf kein [out]-Parameter sein.</dt> <dd> Ein Handle des primitiven Typs <a href="handle-t.md"><strong>handle_t</strong></a> ist nur für die Seite der Anwendung sinnvoll, in der es definiert ist. Der Typ <strong>handle_t</strong> wird nicht im Netzwerk übertragen.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2195"></span><span id="midl2195"></span><dl> <dt><strong>MIDL2195</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_expression_derives_from__unique__or__ptr__pointer_dereference"></span><span id="ATTRIBUTE_EXPRESSION_DERIVES_FROM__UNIQUE__OR__PTR__POINTER_DEREFERENCE"></span>Attributausdruck wird von [unique] oder [ptr] Zeigerdereferenzieren abgeleitet.</dt> <dd> Obwohl die Attribute [<a href="unique.md"><strong>unique</strong></a>] und <a href="ptr.md"><strong>full</strong></a> pointer Zeigern <strong>NULL-Werte</strong> ermöglichen, darf der Ausdruck, der das Größen- oder Längenattribut definiert, nie einen <strong>NULL-Wert</strong> haben. Wenn Zeiger verwendet werden, schränkt MIDL Ausdrücke auf<a href="ref.md"><strong>[ref]-Zeiger</strong></a>ein.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2196"></span><span id="midl2196"></span><dl> <dt><strong>MIDL2196</strong></dt> </dl></td>
<td><dl> <dt><span id="_cpp_quote__requires__ms_ext"></span><span id="_CPP_QUOTE__REQUIRES__MS_EXT"></span>&quot;cpp_quote erfordert &quot; /ms_ext</dt> <dd> Das <a href="cpp-quote.md"><strong>cpp_quote-Attribut</strong></a> ist eine Microsoft-Erweiterung für DCE IDL. Verwenden Sie nicht den MIDL-Compilerschalter <a href="-osf.md"><strong>/osf</strong></a>, der <a href="-ms-ext.md"><strong>/ms_ext</strong></a>überschreibt.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2197"></span><span id="midl2197"></span><dl> <dt><strong>MIDL2197</strong></dt> </dl></td>
<td><dl> <dt><span id="quoted_uuid_requires__ms_ext"></span><span id="QUOTED_UUID_REQUIRES__MS_EXT"></span>uuid in Anführungszeichen erfordert /ms_ext</dt> <dd> Die Möglichkeit, einen UUID-Wert in Anführungszeichen anzugeben, ist eine Microsoft-Erweiterung für DCE IDL. Verwenden Sie nicht den MIDL-Compilerschalter <a href="-osf.md"><strong>/osf</strong></a>, der <a href="-ms-ext.md"><strong>/ms_ext</strong></a>überschreibt.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2198"></span><span id="midl2198"></span><dl> <dt><strong>MIDL2198</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_cannot_derive_from_a_nonencapsulated_union"></span><span id="RETURN_TYPE_CANNOT_DERIVE_FROM_A_NONENCAPSULATED_UNION"></span>Rückgabetyp kann nicht von einer nicht gekapselten Union abgeleitet werden</dt> <dd> Die nicht gekapselte Union kann nicht als Funktionsrückgabetyp verwendet werden. Um den Union-Typ zurückzugeben, geben Sie den Union-Typ als<a href="out-idl.md"><strong>[out]-</strong></a>oder<strong>[in,out]-Parameter</strong>an.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2199"></span><span id="midl2199"></span><dl> <dt><strong>MIDL2199</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_cannot_derive_from_a_conformant_structure"></span><span id="RETURN_TYPE_CANNOT_DERIVE_FROM_A_CONFORMANT_STRUCTURE"></span>Rückgabetyp kann nicht von einer konformen Struktur abgeleitet werden</dt> <dd> Die Größe des Rückgabetyps muss eine Konstante sein. Sie können eine Struktur, die ein konformes Array enthält, nicht als Rückgabetyp angeben, auch wenn die Struktur auch ihren Größenspezifizierer enthält. Um die konforme Struktur zurückzugeben, geben Sie die Struktur als<a href="out-idl.md"><strong>[out]-</strong></a>oder<strong>[in,out]-Parameter</strong>an.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2200"></span><span id="midl2200"></span><dl> <dt><strong>MIDL2200</strong></dt> </dl></td>
<td><dl> <dt><span id="_transmit_as__must_not_be_applied_to_a_type_deriving_from_a_generic_handle"></span><span id="_TRANSMIT_AS__MUST_NOT_BE_APPLIED_TO_A_TYPE_DERIVING_FROM_A_GENERIC_HANDLE"></span>[transmit_as] darf nicht auf einen Typ angewendet werden, der von einem generischen Handle abgeleitet wird.</dt> <dd> In dieser Version können die Attribute [<a href="handle.md"><strong>handle</strong></a>] und [<a href="transmit-as.md"><strong>transmit_as</strong></a>] nicht mit demselben Typ kombiniert werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2201"></span><span id="midl2201"></span><dl> <dt><strong>MIDL2201</strong></dt> </dl></td>
<td><dl> <dt><span id="_handle__must_not_be_applied_to_a_type_that_has__transmit_as__applied_to_it"></span><span id="_HANDLE__MUST_NOT_BE_APPLIED_TO_A_TYPE_THAT_HAS__TRANSMIT_AS__APPLIED_TO_IT"></span>[handle] darf nicht auf einen Typ angewendet werden, auf den [transmit_as] angewendet wurde.</dt> <dd> In dieser Version können die Attribute [<a href="handle.md"><strong>handle</strong></a>] und [<a href="transmit-as.md"><strong>transmit_as</strong></a>] nicht mit demselben Typ kombiniert werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2202"></span><span id="midl2202"></span><dl> <dt><strong>MIDL2202</strong></dt> </dl></td>
<td><dl> <dt><span id="type_specified_for_the_const_declaration_is_invalid"></span><span id="TYPE_SPECIFIED_FOR_THE_CONST_DECLARATION_IS_INVALID"></span>Der für die const-Deklaration angegebene Typ ist ungültig.</dt> <dd> Konstantendeklarationen sind auf Integer-, Zeichen-, Breitzeichen-, Zeichenfolgen- und boolesche Typen beschränkt.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2203"></span><span id="midl2203"></span><dl> <dt><strong>MIDL2203</strong></dt> </dl></td>
<td><dl> <dt><span id="operand_to_the_sizeof_operator_is_not_supported"></span><span id="OPERAND_TO_THE_SIZEOF_OPERATOR_IS_NOT_SUPPORTED"></span>Operand für den sizeof-Operator wird nicht unterstützt.</dt> <dd> Der MIDL-Compiler unterstützt den <strong>sizeof-Vorgang</strong> nur für einfache Typen. Der angegebene Operand wird nicht zu einem ganzzahligen Typ ausgewertet.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2204"></span><span id="midl2204"></span><dl> <dt><strong>MIDL2204</strong></dt> </dl></td>
<td><dl> <dt><span id="this_name_already_used_as_a_const_identifier_name"></span><span id="THIS_NAME_ALREADY_USED_AS_A_CONST_IDENTIFIER_NAME"></span>Dieser Name wird bereits als const-Bezeichnername verwendet.</dt> <dd> Der Bezeichner wurde zuvor verwendet, um eine Konstante in einer <a href="const.md"><strong>const-Deklaration</strong></a> zu identifizieren. Ändern Sie den Namen eines der Bezeichner so, dass die Bezeichner eindeutig sind.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2205"></span><span id="midl2205"></span><dl> <dt><strong>MIDL2205</strong></dt> </dl></td>
<td><dl> <dt><span id="inconsistent_redefinition_of_type_error_status_t"></span><span id="INCONSISTENT_REDEFINITION_OF_TYPE_ERROR_STATUS_T"></span>Inkonsistente Neudefinition des Error_status_t</dt> <dd> Der <a href="error-status-t.md"><strong>typ error_status_t</strong></a> muss in den Typ <strong>unsigned long auflösen.</strong> Andere Typdefinitionen können nicht verwendet werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2206"></span><span id="midl2206"></span><dl> <dt><strong>MIDL2206</strong></dt> </dl></td>
<td><dl> <dt><span id="_case__value_out_of_range_of_switch_type"></span><span id="_CASE__VALUE_OUT_OF_RANGE_OF_SWITCH_TYPE"></span>[case]-Wert liegt nicht im Bereich des Switchtyps.</dt> <dd> Der wert, der dem Fall der switch-Anweisung zugeordnet ist, liegt für den angegebenen Switchtyp nicht im Bereich. Dieser Fehler tritt beispielsweise auf, wenn ein langer ganzzahliger Wert in der case-Anweisung für einen kurzen ganzzahligen Typ verwendet wird.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2207"></span><span id="midl2207"></span><dl> <dt><strong>MIDL2207</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_deriving_from_wchar_t_needs__ms_ext"></span><span id="PARAMETER_DERIVING_FROM_WCHAR_T_NEEDS__MS_EXT"></span>Parameter, der von der wchar_t, benötigt /ms_ext</dt> <dd> Der Breitzeichentyp <a href="wchar-t.md"><strong>wchar_t</strong></a> ist eine Microsoft-Erweiterung für DCE-IDL. Verwenden Sie nicht den MIDL-Compilerschalter <a href="-osf.md"><strong>/osf,</strong></a>der <a href="-ms-ext.md"><strong>/ms_ext</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2208"></span><span id="midl2208"></span><dl> <dt><strong>MIDL2208</strong></dt> </dl></td>
<td><dl> <dt><span id="this_interface_has_only_callbacks"></span><span id="THIS_INTERFACE_HAS_ONLY_CALLBACKS"></span>Diese Schnittstelle verfügt nur über Rückrufe.</dt> <dd> Rückrufe sind nur im Kontext eines Remoteprozeduraufrufs gültig. Die Schnittstelle muss mindestens einen Funktionsprototyp für einen Remoteprozeduraufruf enthalten, der das<a href="callback.md"><strong>[Rückruf]-Attribut</strong></a>nicht enthält.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2209"></span><span id="midl2209"></span><dl> <dt><strong>MIDL2209</strong></dt> </dl></td>
<td><dl> <dt><span id="redundantly_specified_attribute__ignored"></span><span id="REDUNDANTLY_SPECIFIED_ATTRIBUTE__IGNORED"></span>redundant angegebenes Attribut; Ignoriert</dt> <dd> Das angegebene Attribut wurde mehr als einmal angewendet. Mehrere Instanzen desselben Attributs werden ignoriert.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2210"></span><span id="midl2210"></span><dl> <dt><strong>MIDL2210</strong></dt> </dl></td>
<td><dl> <dt><span id="context_handle_type_used_for_an_implicit_handle"></span><span id="CONTEXT_HANDLE_TYPE_USED_FOR_AN_IMPLICIT_HANDLE"></span>Für ein implizites Handle verwendeter Kontexthand handle-Typ</dt> <dd> Ein Typ, der mithilfe des<a href="context-handle.md"><strong>[context_handle</strong></a>]-Attributs definiert wurde, wurde als Handletyp in einem <a href="implicit-handle.md"><strong>[implicit_handle ]-Attribut</strong></a>angegeben. Die Attribute können nicht auf diese Weise kombiniert werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2211"></span><span id="midl2211"></span><dl> <dt><strong>MIDL2211</strong></dt> </dl></td>
<td><dl> <dt><span id="conflicting_options_specified_for__allocate_"></span><span id="CONFLICTING_OPTIONS_SPECIFIED_FOR__ALLOCATE_"></span>In Konflikt stehende Optionen, die für [allocate] angegeben sind</dt> <dd> Die für das ACF-Attribut [<a href="allocate.md"><strong>allocate</strong></a>] angegebenen Optionen stellen in Konflikt stehende Anweisungen dar. Geben Sie beispielsweise entweder die Option all_nodes oder die Option single_node an, aber nicht beides.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2212"></span><span id="midl2212"></span><dl> <dt><strong>MIDL2212</strong></dt> </dl></td>
<td><dl> <dt><span id="error_while_writing_to_file"></span><span id="ERROR_WHILE_WRITING_TO_FILE"></span>Fehler beim Schreiben in eine Datei</dt> <dd> Fehler beim Schreiben in die Datei. Diese Bedingung kann durch Fehler im Zusammenhang mit Speicherplatz, Dateihandles, Dateizugriffseinschränkungen und Hardwarefehlern verursacht werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2213"></span><span id="midl2213"></span><dl> <dt><strong>MIDL2213</strong></dt> </dl></td>
<td><dl> <dt><span id="no_switch_type_found_at_definition_of_union__using_the__switch_is__type"></span><span id="NO_SWITCH_TYPE_FOUND_AT_DEFINITION_OF_UNION__USING_THE__SWITCH_IS__TYPE"></span>Kein Switchtyp in definition of union gefunden, mithilfe des [switch_is]-Typs</dt> <dd> Die Union-Definition enthält kein explizites<a href="switch-type.md"><strong>[switch_type</strong></a>]-Attribut. Der Typ der Variablen, die durch das<a href="switch-is.md"><strong>[switch_is</strong></a>]-Attribut angegeben wird, wird als Switchtyp verwendet.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2214"></span><span id="midl2214"></span><dl> <dt><strong>MIDL2214</strong></dt> </dl></td>
<td><dl> <dt><span id="semantic_check_incomplete_due_to_previous_errors"></span><span id="SEMANTIC_CHECK_INCOMPLETE_DUE_TO_PREVIOUS_ERRORS"></span>Semantikprüfung aufgrund vorheriger Fehler unvollständig</dt> <dd> Der MIDL-Compiler führt zwei Durchläufe über die Eingabedatei(en) durch, um vorwärts Deklarationen aufzulösen. Aufgrund von Fehlern, die während des ersten Durchgangs aufgetreten sind, wurde keine Überprüfung auf den zweiten Durchgang durchgeführt. Nicht gemeldete Fehler im Zusammenhang mit Vorwärtsdeklarationen sind möglicherweise weiterhin in der Datei vorhanden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2215"></span><span id="midl2215"></span><dl> <dt><strong>MIDL2215</strong></dt> </dl></td>
<td><dl> <dt><span id="handle_parameter_or_return_type_is_not_supported_on_a__callback__procedure"></span><span id="HANDLE_PARAMETER_OR_RETURN_TYPE_IS_NOT_SUPPORTED_ON_A__CALLBACK__PROCEDURE"></span>Handleparameter oder Rückgabetyp werden in einer [Rückruf]-Prozedur nicht unterstützt.</dt> <dd> Eine<a href="callback.md"><strong>[Rückruf]-Prozedur</strong></a>tritt im Kontext eines Aufrufs eines Clients an den Server auf und verwendet dasselbe Bindungshand handle wie der ursprüngliche Aufruf. Explizite Bindungshand handle-Parameter oder Rückgabetypen sind in Rückruffunktionen nicht zulässig.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2216"></span><span id="midl2216"></span><dl> <dt><strong>MIDL2216</strong></dt> </dl></td>
<td><dl> <dt><span id="_ptr__does_not_support_aliasing_in_this_version"></span><span id="_PTR__DOES_NOT_SUPPORT_ALIASING_IN_THIS_VERSION"></span>[ptr] unterstützt in dieser Version kein Aliasing.</dt> <dd> Ein Alias tritt auf, wenn auf Daten über mehrere Zeiger- oder Variablennamen zugegriffen werden kann. Entfernen Sie den Alias. Weitere Informationen finden Sie unter <a href="/windows/desktop/Rpc/unique-pointers">Eindeutige Zeiger.</a><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2217"></span><span id="midl2217"></span><dl> <dt><strong>MIDL2217</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_already_defined_as_a_context_handle"></span><span id="PARAMETER_ALREADY_DEFINED_AS_A_CONTEXT_HANDLE"></span>Parameter, der bereits als Kontexthand handle definiert ist</dt> <dd> Der -Parameter wurde zuvor als Kontexthand handle definiert.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2218"></span><span id="midl2218"></span><dl> <dt><strong>MIDL2218</strong></dt> </dl></td>
<td><dl> <dt><span id="_context_handle__must_not_derive_from_handle_t"></span><span id="_CONTEXT_HANDLE__MUST_NOT_DERIVE_FROM_HANDLE_T"></span>[context_handle] darf nicht von der handle_t</dt> <dd> Die drei Handlemerkmale: der Typ <a href="handle-t.md"><strong>handle_t</strong></a>, das Attribut [<a href="handle.md"><strong>Handle</strong></a>] und das Attribut [<a href="context-handle.md"><strong>context_handle</strong></a>], schließen sich gegenseitig aus. Auf einen Typ oder Parameter kann immer nur ein Merkmal angewendet werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2219"></span><span id="midl2219"></span><dl> <dt><strong>MIDL2219</strong></dt> </dl></td>
<td><dl> <dt><span id="array_size_exceeds_65536_bytes"></span><span id="ARRAY_SIZE_EXCEEDS_65536_BYTES"></span>Arraygröße überschreitet 65536 Bytes</dt> <dd> Auf einigen Microsoft-Plattformen beträgt die maximale größe der transmissiblen Daten 64K. Gestalten Sie Ihre Anwendung neu, damit alle übertragenen Daten innerhalb der maximalen transmissiblen Größe passen.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2220"></span><span id="midl2220"></span><dl> <dt><strong>MIDL2220</strong></dt> </dl></td>
<td><dl> <dt><span id="structure_size_exceeds_65536_bytes"></span><span id="STRUCTURE_SIZE_EXCEEDS_65536_BYTES"></span>Strukturgröße überschreitet 65536 Bytes</dt> <dd> Auf einigen Microsoft-Plattformen beträgt die maximale größe der transmissiblen Daten 64K. Gestalten Sie Ihre Anwendung neu, damit alle übertragenen Daten innerhalb der maximalen transmissiblen Größe passen.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2221"></span><span id="midl2221"></span><dl> <dt><strong>MIDL2221</strong></dt> </dl></td>
<td><dl> <dt><span id="field_of_a_nonencapsulated_union_cannot_be_another_nonencapsulated_union"></span><span id="FIELD_OF_A_NONENCAPSULATED_UNION_CANNOT_BE_ANOTHER_NONENCAPSULATED_UNION"></span>Das Feld einer nicht kapselten Union darf keine andere nicht kapselte Union sein.</dt> <dd> Unions, die im Rahmen eines Remoteprozeduraufrufs übertragen werden, erfordern ein zugeordnetes Datenelement, das Diskriminant, das den Union-Arm auswählt. Unions, die in anderen Unions geschachtelt sind, bieten keine Unterscheidung. daher können sie nicht in dieser Form übertragen werden. Erstellen Sie eine -Struktur, die aus der Union und ihrer Diskriminanz besteht.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2222"></span><span id="midl2222"></span><dl> <dt><strong>MIDL2222</strong></dt> </dl></td>
<td><dl> <dt><span id="pointer_attribute_s__applied_on_an_embedded_array__ignored"></span><span id="POINTER_ATTRIBUTE_S__APPLIED_ON_AN_EMBEDDED_ARRAY__IGNORED"></span>Zeigerattribute, die auf ein eingebettetes Array angewendet werden; Ignoriert</dt> <dd> Ein Zeigerattribut kann nur dann auf ein Array angewendet werden, wenn das Array ein Parameter der obersten Ebene ist. Andere Zeigerattribute, die auf Arrays angewendet werden, die in andere Datenstrukturen eingebettet sind, werden ignoriert.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2223"></span><span id="midl2223"></span><dl> <dt><strong>MIDL2223</strong></dt> </dl></td>
<td><dl> <dt><span id="_allocate__is_illegal_on_either_the_transmitted_or_presented_type_for__transmit_as____represent_as____wire_marshal___or__user_marshal_"></span><span id="_ALLOCATE__IS_ILLEGAL_ON_EITHER_THE_TRANSMITTED_OR_PRESENTED_TYPE_FOR__TRANSMIT_AS____REPRESENT_AS____WIRE_MARSHAL___OR__USER_MARSHAL_"></span>[allocate] ist entweder für den übertragenen oder dargestellten Typ für [transmit_as], [represent_as], [wire_marshal] oder [user_marshal] ungültig.</dt> <dd> Die Attribute [<a href="transmit-as.md"><strong>transmit_as</strong></a>] und [<a href="allocate.md"><strong>allocate</strong></a>] können nicht beide auf denselben Typ angewendet werden. Das Attribut [<strong>transmit_as</strong>] unterscheidet zwischen dargestellten und übertragenen Typen, während das Attribut [<strong>allocate</strong>] davon ausgegangen wird, dass der dargestellte Typ mit dem übertragenen Typ identisch ist.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2224"></span><span id="midl2224"></span><dl> <dt><strong>MIDL2224</strong></dt> </dl></td>
<td>[switch_type] muss in diesem Importmodus angegeben werden.<br/></td>
</tr>
<tr class="even">
<td><span id="MIDL2225"></span><span id="midl2225"></span><dl> <dt><strong>MIDL2225</strong></dt> </dl></td>
<td><dl> <dt><span id="_implicit_handle__type_undefined__assuming_generic_handle"></span><span id="_IMPLICIT_HANDLE__TYPE_UNDEFINED__ASSUMING_GENERIC_HANDLE"></span>[implicit_handle] typ undefined; Annahme eines generischen Handles</dt> <dd> Der im ACF angegebene Handletyp ist in der IDL-Datei nicht definiert. Der MIDL-Compiler geht davon aus, dass der Handletyp in den primitiven <a href="handle-t.md"><strong>Handletyp</strong></a>handle_t. Fügen Sie der<a href="handle.md"><strong>Typdefinition</strong></a>das Attribut [ handle ] hinzu, wenn sich das Handle wie ein benutzerdefiniertes oder generisches Handle verhalten soll.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2226"></span><span id="midl2226"></span><dl> <dt><strong>MIDL2226</strong></dt> </dl></td>
<td><dl> <dt><span id="array_element_must_not_derive_from_error_status_t"></span><span id="ARRAY_ELEMENT_MUST_NOT_DERIVE_FROM_ERROR_STATUS_T"></span>Arrayelement darf nicht von der -error_status_t</dt> <dd> In dieser Version von Microsoft RPC kann der <a href="error-status-t.md"><strong>error_status_t</strong></a> nur als Parameter oder Rückgabetyp angezeigt werden. Er kann nicht in Arrays angezeigt werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2227"></span><span id="midl2227"></span><dl> <dt><strong>MIDL2227</strong></dt> </dl></td>
<td><dl> <dt><span id="_allocate__illegal_on_a_type_deriving_from_a_primitive_generic_context_handle"></span><span id="_ALLOCATE__ILLEGAL_ON_A_TYPE_DERIVING_FROM_A_PRIMITIVE_GENERIC_CONTEXT_HANDLE"></span>[allocate] ungültig für einen Typ, der von einem primitiven/generischen/Kontexthand handle ableitung</dt> <dd> Standardmäßig kann das ACF-Attribut [<a href="allocate.md"><strong>allocate</strong></a>] nicht angewendet werden, um Typen zu behandeln.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2228"></span><span id="midl2228"></span><dl> <dt><strong>MIDL2228</strong></dt> </dl></td>
<td><dl> <dt><span id="transmitted_or_presented_type_must_not_derive_from_error_status_t"></span><span id="TRANSMITTED_OR_PRESENTED_TYPE_MUST_NOT_DERIVE_FROM_ERROR_STATUS_T"></span>Der übertragene oder dargestellte Typ darf nicht von einem error_status_t</dt> <dd> In dieser Version von Microsoft RPC kann der <a href="error-status-t.md"><strong>Typ</strong></a> error_status_t nicht mit dem Attribut [<a href="transmit-as.md"><strong>transmit_as</strong></a>] verwendet werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2229"></span><span id="midl2229"></span><dl> <dt><strong>MIDL2229</strong></dt> </dl></td>
<td><dl> <dt><span id="discriminant_of_a_union_must_not_derive_from_a_field_with__ignore__applied_to_it"></span><span id="DISCRIMINANT_OF_A_UNION_MUST_NOT_DERIVE_FROM_A_FIELD_WITH__IGNORE__APPLIED_TO_IT"></span>Diskriminanz einer Union darf nicht von einem Feld ableiten, auf das [ignore] angewendet ist.</dt> <dd> Eine Union, die in einem Remoteprozeduraufruf verwendet wird, muss einem anderen Datenelement zugeordnet werden, das als Diskriminant bezeichnet wird und den Union-Arm auswählt. Die Diskriminanz muss übertragen werden. Das Attribut [<a href="ignore.md"><strong>ignore</strong></a>] kann nicht auf die Union diskriminant angewendet werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2230"></span><span id="midl2230"></span><dl> <dt><strong>MIDL2230</strong></dt> </dl></td>
<td><dl> <dt><span id="_nocode__ignored_for_server_side_since___server_none__not_specified"></span><span id="_NOCODE__IGNORED_FOR_SERVER_SIDE_SINCE___SERVER_NONE__NOT_SPECIFIED"></span>[nocode] für Serverseite ignoriert, &quot; da /server none &quot; nicht angegeben ist</dt> <dd> Einige DCE-IDL-Compiler generieren einen Fehler, wenn das Attribut [<a href="nocode.md"><strong>nocode</strong></a>] auf eine Prozedur in einer Schnittstelle angewendet wird, für die Serverstubdateien generiert werden. Da der Server alle Vorgänge unterstützen muss, darf [<strong>nocode</strong>] nicht auf eine Prozedur in diesem Modus angewendet werden, oder Sie müssen den MIDL-Compilerschalter <a href="-server.md"><strong>/server</strong></a> none verwenden, um explizit anzugeben, dass keine Serverroutinen generiert werden sollen.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2231"></span><span id="midl2231"></span><dl> <dt><strong>MIDL2231</strong></dt> </dl></td>
<td><dl> <dt><span id="no_remote_procedures_specified_in_non-_local__interface__no_client_server_stubs_will_be_generated"></span><span id="NO_REMOTE_PROCEDURES_SPECIFIED_IN_NON-_LOCAL__INTERFACE__NO_CLIENT_SERVER_STUBS_WILL_BE_GENERATED"></span>keine Remoteverfahren, die in der nicht[lokalen] Schnittstelle angegeben sind; Es werden keine Client-/Serverstubs generiert.</dt> <dd> Die bereitgestellte Schnittstelle verfügt nicht über Remoteverfahren, sodass nur Headerdateien generiert werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2232"></span><span id="midl2232"></span><dl> <dt><strong>MIDL2232</strong></dt> </dl></td>
<td><dl> <dt><span id="too_many_default_cases_specified_for_encapsulated_union"></span><span id="TOO_MANY_DEFAULT_CASES_SPECIFIED_FOR_ENCAPSULATED_UNION"></span>Zu viele Standardfälle für gekapselte Union angegeben</dt> <dd> Eine gekapselte Union kann nur einen Standardwert haben: arm.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2233"></span><span id="midl2233"></span><dl> <dt><strong>MIDL2233</strong></dt> </dl></td>
<td><dl> <dt><span id="too_many_default_interfaces_specified_for_coclass"></span><span id="TOO_MANY_DEFAULT_INTERFACES_SPECIFIED_FOR_COCLASS"></span>Zu viele Standardschnittstellen für Co-Klasse angegeben</dt> <dd> Eine <a href="coclass.md"><strong>Co-Klasse</strong></a> kann über mindestens zwei [Standard]-Member verfügen, einen zur Darstellung der ausgehenden Schnittstelle (Quellschnittstelle) oder Disp-Schnittstelle und einen zur Darstellung der eingehenden Schnittstelle (Senke) oder Disp-Schnittstelle.<a href="default.md"><strong></strong></a><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2234"></span><span id="midl2234"></span><dl> <dt><strong>MIDL2234</strong></dt> </dl></td>
<td><dl> <dt><span id="items_with__defaultvtable__must_also_have__source_"></span><span id="ITEMS_WITH__DEFAULTVTABLE__MUST_ALSO_HAVE__SOURCE_"></span>Elemente mit [defaultvtable] müssen ebenfalls über [Quelle] verfügen.</dt> <dd> Die <a href="defaultvtable.md"><strong>defaultvtable-Schnittstelle</strong></a> erstellt eine zweite Quellschnittstelle für ein Objekt, mit der Senken Ereignisse über die V-Tabelle empfangen können.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2235"></span><span id="midl2235"></span><dl> <dt><strong>MIDL2235</strong></dt> </dl></td>
<td><dl> <dt><span id="union_specification_with_no_fields_is_illegal"></span><span id="UNION_SPECIFICATION_WITH_NO_FIELDS_IS_ILLEGAL"></span>Union-Spezifikation ohne Felder ist ungültig</dt> <dd> Unions müssen mindestens ein Feld haben.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2236"></span><span id="midl2236"></span><dl> <dt><strong>MIDL2236</strong></dt> </dl></td>
<td><dl> <dt><span id="value_out_of_range"></span><span id="VALUE_OUT_OF_RANGE"></span>Wert liegt nicht im Bereich</dt> <dd> Der bereitgestellte Fallwert liegt nicht im Bereich des Switchtyps.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2237"></span><span id="midl2237"></span><dl> <dt><strong>MIDL2237</strong></dt> </dl></td>
<td><dl> <dt><span id="_context_handle__must_be_applied_on_a_pointer_type"></span><span id="_CONTEXT_HANDLE__MUST_BE_APPLIED_ON_A_POINTER_TYPE"></span>[context_handle] muss auf einen Zeigertyp angewendet werden.</dt> <dd> Kontexthandles müssen immer Zeigertypen sein. DCE gibt an, dass alle Kontexthandles als void * typ sein <strong>müssen.</strong><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2238"></span><span id="midl2238"></span><dl> <dt><strong>MIDL2238</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_must_not_derive_from_handle_t"></span><span id="RETURN_TYPE_MUST_NOT_DERIVE_FROM_HANDLE_T"></span>Der Rückgabetyp darf nicht von der handle_t</dt> <dd><a href="handle-t.md"><strong>handle_t</strong></a> kann nicht zurückgegeben werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2239"></span><span id="midl2239"></span><dl> <dt><strong>MIDL2239</strong></dt> </dl></td>
<td><dl> <dt><span id="_handle__must_not_be_applied_to_a_type_deriving_from_a_context_handle"></span><span id="_HANDLE__MUST_NOT_BE_APPLIED_TO_A_TYPE_DERIVING_FROM_A_CONTEXT_HANDLE"></span>[Handle] darf nicht auf einen Typ angewendet werden, der von einem Kontexthand handle ableitung.</dt> <dd> Ein Typ kann nicht sowohl ein Kontexthandy als auch ein generisches Handle sein.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2240"></span><span id="midl2240"></span><dl> <dt><strong>MIDL2240</strong></dt> </dl></td>
<td><dl> <dt><span id="field_deriving_from_an__int__must_have_size_specifier__small____short___or__long__with_the__int_"></span><span id="FIELD_DERIVING_FROM_AN__INT__MUST_HAVE_SIZE_SPECIFIER__SMALL____SHORT___OR__LONG__WITH_THE__INT_"></span>Das von einem &quot; int-Element ableitende &quot; Feld muss den Größenspezifizierer &quot; &quot; small, short oder long mit &quot; dem Wert &quot; &quot; &quot; &quot; int haben.&quot;</dt> <dd> Der Typ <a href="int.md"><strong>int</strong></a> ist auf 16-Bit-Systemen nicht transmissierbar, da die Größe von <strong>int</strong> computerübergreifend unterschiedlich sein kann.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2241"></span><span id="midl2241"></span><dl> <dt><strong>MIDL2241</strong></dt> </dl></td>
<td><dl> <dt><span id="field_must_not_derive_from_a_void_or_void__"></span><span id="FIELD_MUST_NOT_DERIVE_FROM_A_VOID_OR_VOID__"></span>feld darf nicht von void oder void *</dt> <dd> <strong>void</strong> und <strong>void * können</strong> nicht als Parametertypen für Remoteverfahren verwendet werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2242"></span><span id="midl2242"></span><dl> <dt><strong>MIDL2242</strong></dt> </dl></td>
<td><dl> <dt><span id="field_must_not_derive_from_a_structure_containing_bit-fields"></span><span id="FIELD_MUST_NOT_DERIVE_FROM_A_STRUCTURE_CONTAINING_BIT-FIELDS"></span>Feld darf nicht von einer Struktur mit Bitfeldern ableiten</dt> <dd> Strukturen, die Bitfelder enthalten, können nicht als Parameter oder Rückgabetypen für Remoteverfahren verwendet werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2243"></span><span id="midl2243"></span><dl> <dt><strong>MIDL2243</strong></dt> </dl></td>
<td><dl> <dt><span id="field_must_not_derive_from_a_non-rpcable_union"></span><span id="FIELD_MUST_NOT_DERIVE_FROM_A_NON-RPCABLE_UNION"></span>Das Feld darf nicht von einer nicht rpcable-Union ableiten.</dt> <dd> Eine Union muss als nicht kapselte Union oder gekapselte Union angegeben werden, um übertragen zu werden. Normalen C-Unions fehlt die Diskriminanz, die erforderlich ist, um die Union über das Netzwerk zu übertragen.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2244"></span><span id="midl2244"></span><dl> <dt><strong>MIDL2244</strong></dt> </dl></td>
<td><dl> <dt><span id="field_must_not_derive_from_a_pointer_to_a_function"></span><span id="FIELD_MUST_NOT_DERIVE_FROM_A_POINTER_TO_A_FUNCTION"></span>Feld darf nicht von einem Zeiger auf eine Funktion ableiten</dt> <dd> Zeiger auf Funktionen können nicht an Remoteverfahren übertragen werden. Zeiger auf Funktionen zeigen auf Funktionscode, und über RPC kann kein Funktionscode über das Netzwerk übertragen werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2245"></span><span id="midl2245"></span><dl> <dt><strong>MIDL2245</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_use__fault_status__on_both_a_parameter_and_a_return_type"></span><span id="CANNOT_USE__FAULT_STATUS__ON_BOTH_A_PARAMETER_AND_A_RETURN_TYPE"></span>[fault_status] kann nicht sowohl für einen Parameter als auch für einen Rückgabetyp verwendet werden.</dt> <dd> Das Attribut [<a href="fault-status.md"><strong>fault_status</strong></a>] kann nur einmal pro Prozedur verwendet werden. Das Attribut [<a href="comm-status.md"><strong>comm_status</strong></a>] kann unabhängig verwendet werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2246"></span><span id="midl2246"></span><dl> <dt><strong>MIDL2246</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_too_complicated_for__Oi_modes__using__Os"></span><span id="return_type_too_complicated_for__oi_modes__using__os"></span><span id="RETURN_TYPE_TOO_COMPLICATED_FOR__OI_MODES__USING__OS"></span>Rückgabetyp für /Oi-Modi mit /Os zu kompliziert</dt> <dd> Große Rückgabetypen, die als Wert übergeben <a href="-os.md"><strong></strong></a> werden, können nur von /Os-Optimierungstubs verarbeitet werden. Die Stubs für diese Routine werden mithilfe der <strong>/Os-Optimierung</strong> generiert.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2247"></span><span id="midl2247"></span><dl> <dt><strong>MIDL2247</strong></dt> </dl></td>
<td><dl> <dt><span id="generic_handle_type_too_large_for__Oi_modes__using__Os"></span><span id="generic_handle_type_too_large_for__oi_modes__using__os"></span><span id="GENERIC_HANDLE_TYPE_TOO_LARGE_FOR__OI_MODES__USING__OS"></span>Generischer Handletyp für /Oi-Modi zu groß mit /Os</dt> <dd> Große generische Handletypen, die als Wert übergeben <a href="-os.md"><strong></strong></a> werden, können nur von /Os-Optimierungstubs verarbeitet werden. Die Stubs für diese Routine werden mithilfe der <strong>/Os-Optimierung</strong> generiert.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2248"></span><span id="midl2248"></span><dl> <dt><strong>MIDL2248</strong></dt> </dl></td>
<td><dl> <dt><span id="_allocate_all_nodes___on_an__in_out__parameter_may_orphan_the_original_memory"></span><span id="_ALLOCATE_ALL_NODES___ON_AN__IN_OUT__PARAMETER_MAY_ORPHAN_THE_ORIGINAL_MEMORY"></span>[allocate(all_nodes)] für einen [in,out]-Parameter kann den ursprünglichen Speicher verwaisten.</dt> <dd> Die Verwendung von [<a href="allocate.md"><strong>allocate</strong></a>(all_nodes)] für einen [<a href="in.md"><strong>in</strong></a>, <a href="out-idl.md"><strong>out</strong></a>] -Parameter muss zusammenhängenden Speicher für die [<strong>out</strong>]-Richtung neu zuordnen, wodurch der [<strong>in</strong>] -Parameter verwaist wird. Diese Verwendung wird nicht empfohlen.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2249"></span><span id="midl2249"></span><dl> <dt><strong>MIDL2249</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_have_a__ref__pointer_as_a_union_arm"></span><span id="CANNOT_HAVE_A__REF__POINTER_AS_A_UNION_ARM"></span>kann keinen [ref]-Zeiger als Union-Arm haben.</dt> <dd> Verweiszeiger müssen immer auf gültigen Speicher zeigen, aber eine Union [<a href="in.md"><strong>in</strong></a>, <a href="out-idl.md"><strong>out</strong></a>] mit einem Verweiszeiger kann einen Verweiszeiger zurückgeben, wenn die [<strong>in</strong>] -Richtung einen anderen Typ verwendet hat.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2250"></span><span id="midl2250"></span><dl> <dt><strong>MIDL2250</strong></dt> </dl></td>
<td><dl> <dt><span id="return_of_context_handles_not_supported_for__Oi_modes__using__Os"></span><span id="return_of_context_handles_not_supported_for__oi_modes__using__os"></span><span id="RETURN_OF_CONTEXT_HANDLES_NOT_SUPPORTED_FOR__OI_MODES__USING__OS"></span>Rückgabe von Kontexthandles, die für /Oi-Modi nicht unterstützt werden, mit /Os</dt> <dd> MIDL unterstützt keine Kontexthandles in den vollständig interpretierten Optimierungsmodi. Wechsel zur Optimierung im gemischten Modus.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2251"></span><span id="midl2251"></span><dl> <dt><strong>MIDL2251</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_the_extra__comm_status__or__fault_status__parameter_not_supported_for__Oi_modes__using__Os"></span><span id="use_of_the_extra__comm_status__or__fault_status__parameter_not_supported_for__oi_modes__using__os"></span><span id="USE_OF_THE_EXTRA__COMM_STATUS__OR__FAULT_STATUS__PARAMETER_NOT_SUPPORTED_FOR__OI_MODES__USING__OS"></span>Verwendung des zusätzlichen [comm_status] oder [fault_status]-Parameters, der für /Oi-Modi nicht unterstützt wird, mithilfe von /Os</dt> <dd> Die Attribute [<a href="comm-status.md"><strong>comm_status</strong></a>] und [<a href="fault-status.md"><strong>fault_status</strong></a>] können nur von /Os-Optimierungstubs verarbeitet werden. <a href="-os.md"><strong></strong></a> Die Stubs für diese Routine werden mithilfe der <strong>/Os-Optimierung</strong> generiert.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2252"></span><span id="midl2252"></span><dl> <dt><strong>MIDL2252</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_an_unknown_type_for__represent_as__or__user_marshal__not_supported_for__Oi_modes__using__Os"></span><span id="use_of_an_unknown_type_for__represent_as__or__user_marshal__not_supported_for__oi_modes__using__os"></span><span id="USE_OF_AN_UNKNOWN_TYPE_FOR__REPRESENT_AS__OR__USER_MARSHAL__NOT_SUPPORTED_FOR__OI_MODES__USING__OS"></span>Die Verwendung eines unbekannten Typs für [represent_as] oder [user_marshal] wird für /Oi-Modi mit /Os nicht unterstützt.</dt> <dd> Die Verwendung des Attributs [<a href="represent-as.md"><strong>represent_as</strong></a>] mit einem lokalen Typ, der nicht in der IDL-Datei oder einer importierten IDL-Datei definiert ist, kann nur von /Os-Optimierungstubs verarbeitet werden. <a href="-os.md"><strong></strong></a> Die Stubs für diese Routine werden mithilfe der <strong>/Os-Optimierung</strong> generiert.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2253"></span><span id="midl2253"></span><dl> <dt><strong>MIDL2253</strong></dt> </dl></td>
<td><dl> <dt><span id="array_types_with__transmit_as__or__represent_as__not_supported_on_return_type_for__Oi_modes___using__Os"></span><span id="array_types_with__transmit_as__or__represent_as__not_supported_on_return_type_for__oi_modes___using__os"></span><span id="ARRAY_TYPES_WITH__TRANSMIT_AS__OR__REPRESENT_AS__NOT_SUPPORTED_ON_RETURN_TYPE_FOR__OI_MODES___USING__OS"></span>Arraytypen mit [transmit_as] oder [represent_as] werden für den Rückgabetyp für /Oi-Modi mit /Os nicht unterstützt.</dt> <dd> Die Rückgabe eines Arrays mit [<a href="transmit-as.md"><strong>transmit_as</strong></a>] oder [<a href="represent-as.md"><strong>represent_as</strong></a>] kann nur von /Os-Optimierungstubs verarbeitet werden. <a href="-os.md"><strong></strong></a> Die Stubs für diese Routine werden mithilfe der <strong>/Os-Optimierung</strong> generiert.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2254"></span><span id="midl2254"></span><dl> <dt><strong>MIDL2254</strong></dt> </dl></td>
<td><dl> <dt><span id="array_types_with__transmit_as__or__represent_as__not_supported_pass-by-value_for__Oi_modes__using__Os"></span><span id="array_types_with__transmit_as__or__represent_as__not_supported_pass-by-value_for__oi_modes__using__os"></span><span id="ARRAY_TYPES_WITH__TRANSMIT_AS__OR__REPRESENT_AS__NOT_SUPPORTED_PASS-BY-VALUE_FOR__OI_MODES__USING__OS"></span>Arraytypen mit [transmit_as] oder [represent_as] werden für /Oi-Modi nicht unterstützt, indem /Os verwendet wird.</dt> <dd> Diese Aktion wird für die vollständig interpretierte Optimierung nicht unterstützt. Wechsel zur Optimierung im gemischten Modus.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2255"></span><span id="midl2255"></span><dl> <dt><strong>MIDL2255</strong></dt> </dl></td>
<td><dl> <dt><span id="_callback__requires__ms_ext"></span><span id="_CALLBACK__REQUIRES__MS_EXT"></span>[Rückruf] erfordert /ms_ext</dt> <dd> Das Attribut [<a href="callback.md"><strong>callback</strong></a>] ist eine Microsoft-Erweiterung und erfordert, dass <a href="-ms-ext.md"><strong>der Schalter /ms_ext</strong></a> aktiviert ist. Kompilieren Sie nicht <a href="-osf.md"><strong>mit /osf,</strong></a>wodurch <strong>/ms_ext.</strong><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2256"></span><span id="midl2256"></span><dl> <dt><strong>MIDL2256</strong></dt> </dl></td>
<td><dl> <dt><span id="circular_interface_dependency"></span><span id="CIRCULAR_INTERFACE_DEPENDENCY"></span>Ringschnittstellenabhängigkeit</dt> <dd> Diese Schnittstelle verwendet sich selbst (direkt oder indirekt) als Basisschnittstelle.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2257"></span><span id="midl2257"></span><dl> <dt><strong>MIDL2257</strong></dt> </dl></td>
<td><dl> <dt><span id="only_IUnknown_may_be_used_as_the_root_interface"></span><span id="only_iunknown_may_be_used_as_the_root_interface"></span><span id="ONLY_IUNKNOWN_MAY_BE_USED_AS_THE_ROOT_INTERFACE"></span>nur IUnknown kann als Stammschnittstelle verwendet werden.</dt> <dd> Derzeit müssen alle Schnittstellen <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown als</strong></a> Stammschnittstelle haben.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2258"></span><span id="midl2258"></span><dl> <dt><strong>MIDL2258</strong></dt> </dl></td>
<td><dl> <dt><span id="_IID_IS__may_only_be_applied_to_pointers_to_interfaces"></span><span id="_iid_is__may_only_be_applied_to_pointers_to_interfaces"></span><span id="_IID_IS__MAY_ONLY_BE_APPLIED_TO_POINTERS_TO_INTERFACES"></span>[IID_IS] kann nur auf Zeiger auf Schnittstellen angewendet werden.</dt> <dd> Das Attribut [<a href="iid-is.md"><strong>iid_is</strong></a>] kann nur auf Schnittstellenzeker angewendet werden, obwohl sie als Zeiger auf <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown * angegeben werden</strong></a> können.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2259"></span><span id="midl2259"></span><dl> <dt><strong>MIDL2259</strong></dt> </dl></td>
<td><dl> <dt><span id="interfaces_may_only_be_used_in_pointer-to-interface_constructs"></span><span id="INTERFACES_MAY_ONLY_BE_USED_IN_POINTER-TO-INTERFACE_CONSTRUCTS"></span>Schnittstellen dürfen nur in Zeiger-zu-Schnittstellen-Konstrukten verwendet werden.</dt> <dd> Schnittstellennamen können nur als Basisschnittstellen oder Schnittstellenzeker verwendet werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2260"></span><span id="midl2260"></span><dl> <dt><strong>MIDL2260</strong></dt> </dl></td>
<td><dl> <dt><span id="interface_pointers_must_have_a_UUID_IID"></span><span id="interface_pointers_must_have_a_uuid_iid"></span><span id="INTERFACE_POINTERS_MUST_HAVE_A_UUID_IID"></span>Schnittstellenzeker müssen über eine UUID/IID verfügen.</dt> <dd> Der Basistyp des<a href="iid-is.md"><strong>[iid_is</strong></a>] -Ausdrucks muss ein UUID-/GUID-/IID-Typ sein.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2261"></span><span id="midl2261"></span><dl> <dt><strong>MIDL2261</strong></dt> </dl></td>
<td><dl> <dt><span id="definitions_and_declarations_outside_of_interface_body_requires__ms_ext"></span><span id="DEFINITIONS_AND_DECLARATIONS_OUTSIDE_OF_INTERFACE_BODY_REQUIRES__MS_EXT"></span>Definitionen und Deklarationen außerhalb des Schnittstellenkörpers erfordern /ms_ext</dt> <dd> Das Setzen von Deklarationen und Definitionen außerhalb eines Schnittstellenkörpers ist eine Microsoft-Erweiterung und erfordert die Verwendung des <a href="-ms-ext.md"><strong>Schalters /ms_ext.</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2262"></span><span id="midl2262"></span><dl> <dt><strong>MIDL2262</strong></dt> </dl></td>
<td><dl> <dt><span id="multiple_interfaces_in_one_file_requires__ms_ext"></span><span id="MULTIPLE_INTERFACES_IN_ONE_FILE_REQUIRES__MS_EXT"></span>für mehrere Schnittstellen in einer Datei ist /ms_ext</dt> <dd> Die Verwendung mehrerer Schnittstellen in einer einzelnen iDL-Datei ist eine Microsoft-Erweiterung und nicht verfügbar, wenn Sie im <a href="-osf.md"><strong>/osf-Modus kompilieren.</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2263"></span><span id="midl2263"></span><dl> <dt><strong>MIDL2263</strong></dt> </dl></td>
<td><dl> <dt><span id="only_one_of__implicit_handle____auto_handle___or__explicit_handle__allowed"></span><span id="ONLY_ONE_OF__IMPLICIT_HANDLE____AUTO_HANDLE___OR__EXPLICIT_HANDLE__ALLOWED"></span>Nur einer von [implicit_handle], [auto_handle] oder [explicit_handle] ist zulässig.</dt> <dd> Jede Schnittstelle kann nur eines dieser drei Attribute haben.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2264"></span><span id="midl2264"></span><dl> <dt><strong>MIDL2264</strong></dt> </dl></td>
<td><dl> <dt><span id="_implicit_handle__references_a_type_which_is_not_a_handle"></span><span id="_IMPLICIT_HANDLE__REFERENCES_A_TYPE_WHICH_IS_NOT_A_HANDLE"></span>[implicit_handle] verweist auf einen Typ, der kein Handle ist.</dt> <dd> Implizite Handles müssen einen der Handletypen haben.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2265"></span><span id="midl2265"></span><dl> <dt><strong>MIDL2265</strong></dt> </dl></td>
<td><dl> <dt><span id="_object__procs_may_only_be_used_with___env_win32_"></span><span id="_OBJECT__PROCS_MAY_ONLY_BE_USED_WITH___ENV_WIN32_"></span>[Objekt] -Procs dürfen nur mit &quot; /env win32 verwendet werden.&quot;</dt> <dd> Schnittstellen mit dem<a href="object.md"><strong>[Object</strong></a>]-Attribut können nicht mit 16-Bit-Umgebungen verwendet werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2266"></span><span id="midl2266"></span><dl> <dt><strong>MIDL2266</strong></dt> </dl></td>
<td><dl> <dt><span id="_callback__with_-env_dos_win16_not_supported_for__Oi__using__Os"></span><span id="_callback__with_-env_dos_win16_not_supported_for__oi__using__os"></span><span id="_CALLBACK__WITH_-ENV_DOS_WIN16_NOT_SUPPORTED_FOR__OI__USING__OS"></span>[Rückruf] mit -env dos/win16 wird für /Oi nicht unterstützt, mithilfe von /Os</dt> <dd> Rückrufe in 16-Bit-Umgebungen können nur von /Os-Optimierungstubs verarbeitet werden. <a href="-os.md"><strong></strong></a> Die Stubs für diese Routine werden mithilfe der <strong>/Os-Optimierung</strong> generiert.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2267"></span><span id="midl2267"></span><dl> <dt><strong>MIDL2267</strong></dt> </dl></td>
<td><dl> <dt><span id="float_double_not_supported_as_top-level_parameter_for__Oi_mode__using__Os"></span><span id="float_double_not_supported_as_top-level_parameter_for__oi_mode__using__os"></span><span id="FLOAT_DOUBLE_NOT_SUPPORTED_AS_TOP-LEVEL_PARAMETER_FOR__OI_MODE__USING__OS"></span>float/double wird nicht als Parameter der obersten Ebene für den /Oi-Modus mit /Os unterstützt.</dt> <dd> Die Typen float und double können nur <a href="-os.md"><strong></strong></a> von den /Os-Optimierungstubs als Parameter behandelt werden. Die Stubs für diese Routine werden mithilfe der <strong>/Os-Optimierung</strong> generiert. Die Typen float und double innerhalb von Strukturen, Arrays oder Unions können weiterhin mit<strong>/Os behandelt werden.</strong><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2268"></span><span id="midl2268"></span><dl> <dt><strong>MIDL2268</strong></dt> </dl></td>
<td><dl> <dt><span id="pointers_to_context_handles_may_not_be_used_as_return_values"></span><span id="POINTERS_TO_CONTEXT_HANDLES_MAY_NOT_BE_USED_AS_RETURN_VALUES"></span>Zeiger auf Kontexthandles dürfen nicht als Rückgabewerte verwendet werden.</dt> <dd> Kontexthandles müssen als direkte Rückgabewerte und nicht als indirekte Rückgabewerte verwendet werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2269"></span><span id="midl2269"></span><dl> <dt><strong>MIDL2269</strong></dt> </dl></td>
<td><dl> <dt><span id="procedures_in_an_object_interface_must_return_an_HRESULT"></span><span id="procedures_in_an_object_interface_must_return_an_hresult"></span><span id="PROCEDURES_IN_AN_OBJECT_INTERFACE_MUST_RETURN_AN_HRESULT"></span>Prozeduren in einer Objektschnittstelle müssen ein HRESULT zurückgeben.</dt> <dd> Alle Prozeduren in einer Objektschnittstelle, die nicht über das -[<a href="local.md"><strong>local</strong></a>]-Attribut verfügen, müssen <strong>einen HRESULT</strong> / <strong>SCODE zurückgeben.</strong><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2270"></span><span id="midl2270"></span><dl> <dt><strong>MIDL2270</strong></dt> </dl></td>
<td><dl> <dt><span id="duplicate_UUID"></span><span id="duplicate_uuid"></span><span id="DUPLICATE_UUID"></span>Doppelte UUID</dt> <dd> Identisch mit UUIDs muss eindeutig sein.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2271"></span><span id="midl2271"></span><dl> <dt><strong>MIDL2271</strong></dt> </dl></td>
<td><dl> <dt><span id="_object__interfaces_must_derive_from_another__object__interface_such_as_IUnknown"></span><span id="_object__interfaces_must_derive_from_another__object__interface_such_as_iunknown"></span><span id="_OBJECT__INTERFACES_MUST_DERIVE_FROM_ANOTHER__OBJECT__INTERFACE_SUCH_AS_IUNKNOWN"></span>[Objekt] Schnittstellen müssen von einer anderen [Objekt]-Schnittstelle wie IUnknown ableiten.</dt> <dd> Schnittstellenvererbung ist nur zulässig, wenn Sie Objektschnittstellen verwenden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2272"></span><span id="midl2272"></span><dl> <dt><strong>MIDL2272</strong></dt> </dl></td>
<td><dl> <dt><span id="_async__interface_must_derive_from_another__async__interface"></span><span id="_ASYNC__INTERFACE_MUST_DERIVE_FROM_ANOTHER__ASYNC__INTERFACE"></span>(asynchrone) Schnittstelle muss von einer anderen (asynchronen) Schnittstelle ableiten</dt> <dd> Sowohl synchrone als auch asynchrone Objektschnittstellen müssen von <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a> oder einer anderen OLE-Basisschnittstelle ableiten.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2273"></span><span id="midl2273"></span><dl> <dt><strong>MIDL2273</strong></dt> </dl></td>
<td><dl> <dt><span id="_IID_IS__expression_must_be_a_pointer_to_IID_structure"></span><span id="_iid_is__expression_must_be_a_pointer_to_iid_structure"></span><span id="_IID_IS__EXPRESSION_MUST_BE_A_POINTER_TO_IID_STRUCTURE"></span>[IID_IS]-Ausdruck muss ein Zeiger auf die IID-Struktur sein.</dt> <dd> Der Basistyp des<a href="iid-is.md"><strong>[iid_is</strong></a>] -Ausdrucks muss ein UUID-/GUID-/IID-Typ sein.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2274"></span><span id="midl2274"></span><dl> <dt><strong>MIDL2274</strong></dt> </dl></td>
<td><dl> <dt><span id="_call_as__type_must_be_a__local__procedure"></span><span id="_CALL_AS__TYPE_MUST_BE_A__LOCAL__PROCEDURE"></span>[call_as]-Typ muss eine [lokale] Prozedur sein.</dt> <dd> Auf das Ziel eines<a href="call-as.md"><strong>[call_as]-Typs</strong></a>muss [ <a href="local.md"><strong>local</strong></a>] angewendet sein, sofern definiert.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2275"></span><span id="midl2275"></span><dl> <dt><strong>MIDL2275</strong></dt> </dl></td>
<td><dl> <dt><span id="undefined__call_as__must_not_be_used_in_an_object_interface"></span><span id="UNDEFINED__CALL_AS__MUST_NOT_BE_USED_IN_AN_OBJECT_INTERFACE"></span>Undefined [call_as] darf nicht in einer Objektschnittstelle verwendet werden</dt> <dd> Sie müssen das Ziel eines [call_as<a href="call-as.md"><strong>]-Typs</strong></a>definieren. Stellen Sie sicher, dass <strong>Sie call_as</strong> für die aufrufenden und aufgerufenen Anwendungen bereitgestellt haben.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2276"></span><span id="midl2276"></span><dl> <dt><strong>MIDL2276</strong></dt> </dl></td>
<td><dl> <dt><span id="_auto_handle__may_not_be_used_with__encode__or__decode_"></span><span id="_AUTO_HANDLE__MAY_NOT_BE_USED_WITH__ENCODE__OR__DECODE_"></span>[auto_handle] darf nicht mit [encode] oder [decode] verwendet werden.</dt> <dd> Die Attribute [ <a href="encode.md"><strong>encode</strong></a>] und [ <a href="decode.md"><strong>decode</strong></a>] können nur mit expliziten Handles oder impliziten Handles verwendet werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2277"></span><span id="midl2277"></span><dl> <dt><strong>MIDL2277</strong></dt> </dl></td>
<td><dl> <dt><span id="normal_procedures_are_not_allowed_in_an_interface_with__encode__or__decode_"></span><span id="NORMAL_PROCEDURES_ARE_NOT_ALLOWED_IN_AN_INTERFACE_WITH__ENCODE__OR__DECODE_"></span>Normale Prozeduren sind in einer Schnittstelle mit [Encode] oder [decode] nicht zulässig.</dt> <dd> Schnittstellen, die [<a href="encode.md"><strong>encode</strong></a>] oder [<a href="decode.md"><strong>decode</strong></a>] -Prozeduren enthalten, können keine Remoteverfahren enthalten.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2278"></span><span id="midl2278"></span><dl> <dt><strong>MIDL2278</strong></dt> </dl></td>
<td><dl> <dt><span id="top-level_conformance_or_variance_not_allowed_with__encode__or__decode_"></span><span id="TOP-LEVEL_CONFORMANCE_OR_VARIANCE_NOT_ALLOWED_WITH__ENCODE__OR__DECODE_"></span>Übereinstimmung oder Varianz der obersten Ebene ist bei [Codierung] oder [Decodierung] nicht zulässig.</dt> <dd> Typen mit Übereinstimmung auf oberster Ebene oder Varianz können die Typserialisierung nicht verwenden, da es keine Möglichkeit gibt, größen- bzw. längenrierend zu sein. Strukturen, die sie enthalten, dürfen jedoch die Typserialisierung verwenden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2279"></span><span id="midl2279"></span><dl> <dt><strong>MIDL2279</strong></dt> </dl></td>
<td><dl> <dt><span id="_out__parameters_may_not_have__const_"></span><span id="_OUT__PARAMETERS_MAY_NOT_HAVE__CONST_"></span>[out]-Parameter verfügen möglicherweise nicht &quot; über const.&quot;</dt> <dd> Da ein [<a href="out-idl.md"><strong>out</strong></a>] -Parameter geändert wird, darf er nicht als sa-Konstante deklariert werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2280"></span><span id="midl2280"></span><dl> <dt><strong>MIDL2280</strong></dt> </dl></td>
<td><dl> <dt><span id="return_values_may_not_have__const_"></span><span id="RETURN_VALUES_MAY_NOT_HAVE__CONST_"></span>Rückgabewerte verfügen möglicherweise nicht über &quot; const.&quot;</dt> <dd> Da ein Funktionswert festgelegt wird, wenn die Funktion zurückgegeben wird, darf dieser Wert nicht als Konstante deklariert werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2281"></span><span id="midl2281"></span><dl> <dt><strong>MIDL2281</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid_use_of__retval__attribute"></span><span id="INVALID_USE_OF__RETVAL__ATTRIBUTE"></span>Ungültige Verwendung des &quot; Retval-Attributs &quot;</dt> <dd> Stellen Sie sicher, dass Sie das<a href="optional.md"><strong>[optional</strong></a>] -Attribut nicht verwendet haben und dass der<a href="retval.md"><strong>[retval</strong></a>]-Parameter der letzte Parameter in der Liste ist.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2282"></span><span id="midl2282"></span><dl> <dt><strong>MIDL2282</strong></dt> </dl></td>
<td><dl> <dt><span id="multiple_calling_conventions_illegal"></span><span id="MULTIPLE_CALLING_CONVENTIONS_ILLEGAL"></span>Mehrere Aufrufkonventionen sind unzulässig.</dt> <dd> Nur eine Aufrufkonvention kann auf eine einzelne Prozedur angewendet werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2283"></span><span id="midl2283"></span><dl> <dt><strong>MIDL2283</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_illegal_on__object__procedure"></span><span id="ATTRIBUTE_ILLEGAL_ON__OBJECT__PROCEDURE"></span>Attribut für [Objekt]-Prozedur ungültig</dt> <dd> Das obige Attribut gilt nur für Prozeduren in Schnittstellen, die nicht über das Attribut [<a href="object.md"><strong>object</strong></a>] verfügen.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2284"></span><span id="midl2284"></span><dl> <dt><strong>MIDL2284</strong></dt> </dl></td>
<td><dl> <dt><span id="_out__interface_pointers_must_use_double_indirection"></span><span id="_OUT__INTERFACE_POINTERS_MUST_USE_DOUBLE_INDIRECTION"></span>[out] Schnittstellenzeker müssen doppelte Deskription verwenden.</dt> <dd> Da der geänderte Wert der Zeiger auf die Schnittstelle ist, muss über dem Zeiger eine weitere Deskriptionsebene angegeben werden, damit er zurückgegeben werden kann.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2285"></span><span id="midl2285"></span><dl> <dt><strong>MIDL2285</strong></dt> </dl></td>
<td><dl> <dt><span id="procedure_used_twice_as_the_caller_in__call_as_"></span><span id="PROCEDURE_USED_TWICE_AS_THE_CALLER_IN__CALL_AS_"></span>Prozedur, die zweimal als Aufrufer in [call_as] verwendet wird</dt> <dd> Eine bestimmte [<a href="local.md"><strong>local</strong></a>] -Prozedur kann nur einmal als Ziel einer<a href="call-as.md"><strong>[call_as</strong></a>] verwendet werden, um Namenskonflikte zu vermeiden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2286"></span><span id="midl2286"></span><dl> <dt><strong>MIDL2286</strong></dt> </dl></td>
<td><dl> <dt><span id="_call_as__target_must_have__local__in_an_object_interface"></span><span id="_CALL_AS__TARGET_MUST_HAVE__LOCAL__IN_AN_OBJECT_INTERFACE"></span>[call_as]-Ziel muss [local] in einer Objektschnittstelle haben.</dt> <dd> Das Ziel einer [<a href="call-as.md"><strong>call_as</strong></a>] muss eine definierte [<a href="local.md"><strong>local</strong></a>] -Prozedur in der aktuellen Schnittstelle sein.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2287"></span><span id="midl2287"></span><dl> <dt><strong>MIDL2287</strong></dt> </dl></td>
<td><dl> <dt><span id="_code__and__nocode__may_not_be_used_together"></span><span id="_CODE__AND__NOCODE__MAY_NOT_BE_USED_TOGETHER"></span>[code] und [nocode] dürfen nicht zusammen verwendet werden.</dt> <dd> Diese beiden Attribute sind unentsprichtlich und können nicht zusammen verwendet werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2288"></span><span id="midl2288"></span><dl> <dt><strong>MIDL2288</strong></dt> </dl></td>
<td><dl> <dt><span id="procedures_with__maybe__or__message__attributes_may_not_have__out__params__or_return_values_must_be_of_type_HRESULT_or_error_status_t"></span><span id="procedures_with__maybe__or__message__attributes_may_not_have__out__params__or_return_values_must_be_of_type_hresult_or_error_status_t"></span><span id="PROCEDURES_WITH__MAYBE__OR__MESSAGE__ATTRIBUTES_MAY_NOT_HAVE__OUT__PARAMS__OR_RETURN_VALUES_MUST_BE_OF_TYPE_HRESULT_OR_ERROR_STATUS_T"></span>Prozeduren mit [maybe]- oder [message]-Attributen verfügen möglicherweise nicht über [out]-Parameter, oder Rückgabewerte müssen vom Typ HRESULT oder error_status_t</dt> <dd> Da [<a href="maybe.md"><strong>maybe</strong></a>] -Prozeduren nie zurückgeben, gibt es keine Möglichkeit, Rückgabewerte zu erhalten.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2289"></span><span id="midl2289"></span><dl> <dt><strong>MIDL2289</strong></dt> </dl></td>
<td><dl> <dt><span id="pointer_to_function_must_be_used"></span><span id="POINTER_TO_FUNCTION_MUST_BE_USED"></span>Zeiger auf Funktion muss verwendet werden</dt> <dd> Obwohl Funktionstypdefinitionen im <a href="-c-ext.md"><strong>/c_ext-Modus</strong></a> zulässig sind, können sie nur als Zeiger auf Funktionen verwendet werden. Sie können nie als Parameter oder Rückgabewert einer Remoteprozedur übertragen werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2290"></span><span id="midl2290"></span><dl> <dt><strong>MIDL2290</strong></dt> </dl></td>
<td><dl> <dt><span id="functions_may_not_be_passed_in_an_RPC_operation"></span><span id="functions_may_not_be_passed_in_an_rpc_operation"></span><span id="FUNCTIONS_MAY_NOT_BE_PASSED_IN_AN_RPC_OPERATION"></span>-Funktionen werden in einem RPC-Vorgang möglicherweise nicht übergeben.</dt> <dd> Funktionen und Funktionszeduren können nicht als Parameter oder Rückgabewerte von Remoteverfahren übergeben werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2291"></span><span id="midl2291"></span><dl> <dt><strong>MIDL2291</strong></dt> </dl></td>
<td><dl> <dt><span id="hyper_double_not_supported_as_return_value_for__Oi_modes__using__Os"></span><span id="hyper_double_not_supported_as_return_value_for__oi_modes__using__os"></span><span id="HYPER_DOUBLE_NOT_SUPPORTED_AS_RETURN_VALUE_FOR__OI_MODES__USING__OS"></span>hyper/double wird nicht als Rückgabewert für /Oi-Modi mit /Os unterstützt.</dt> <dd> Hyper- und double-Rückgabewerte können <a href="-os.md"><strong></strong></a> nur von /Os-Optimierungstubs verarbeitet werden. Die Stubs für diese Routine werden mithilfe der <strong>/Os-Optimierung</strong> generiert.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2292"></span><span id="midl2292"></span><dl> <dt><strong>MIDL2292</strong></dt> </dl></td>
<td><dl> <dt><span id="_pragma_pack_pop__without_matching__pragma_pack_push_"></span><span id="_PRAGMA_PACK_POP__WITHOUT_MATCHING__PRAGMA_PACK_PUSH_"></span>#pragma pack(pop) without matching #pragma pack(push)</dt> <dd> #pragma pack(push) und #pragma pack(pop) müssen in übereinstimmenden Paaren angezeigt werden. Mindestens eine zu viele #pragma paket(push)s wurden angegeben.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2293"></span><span id="midl2293"></span><dl> <dt><strong>MIDL2293</strong></dt> </dl></td>
<td><dl> <dt><span id="stringable_structure_fields_must_be_byte_char_wchar_t"></span><span id="STRINGABLE_STRUCTURE_FIELDS_MUST_BE_BYTE_CHAR_WCHAR_T"></span>Zeichenfolgen-Strukturfelder müssen byte/char/wchar_t</dt> <dd> Der Typ [<a href="string.md"><strong>string</strong></a>] kann nur auf eine Struktur angewendet werden, deren Felder alle vom Typ Byte sind, oder auf eine Typdefinition, die byte entspricht.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2294"></span><span id="midl2294"></span><dl> <dt><strong>MIDL2294</strong></dt> </dl></td>
<td><dl> <dt><span id="_notify__not_supported_for__Oi_modes__using__Os"></span><span id="_notify__not_supported_for__oi_modes__using__os"></span><span id="_NOTIFY__NOT_SUPPORTED_FOR__OI_MODES__USING__OS"></span>[notify] wird für /Oi-Modi mit /Os nicht unterstützt.</dt> <dd> Das Attribut [<a href="notify.md"><strong>notify</strong></a>] kann nur von /Os-Optimierungstubs verarbeitet werden. <a href="-os.md"><strong></strong></a><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2295"></span><span id="midl2295"></span><dl> <dt><strong>MIDL2295</strong></dt> </dl></td>
<td><dl> <dt><span id="_handle_parameter_or_return_type_is_not_supported_on_a_procedure_in_an__object__interface"></span><span id="_HANDLE_PARAMETER_OR_RETURN_TYPE_IS_NOT_SUPPORTED_ON_A_PROCEDURE_IN_AN__OBJECT__INTERFACE"></span> Handleparameter oder Rückgabetyp werden für eine Prozedur in einer [Objekt]-Schnittstelle nicht unterstützt.</dt> <dd> Handles können nicht mit <a href="object.md"><strong>[Objekt]-Schnittstellen</strong></a>verwendet werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2296"></span><span id="midl2296"></span><dl> <dt><strong>MIDL2296</strong></dt> </dl></td>
<td><dl> <dt><span id="ANSI_C_only_allows_the_leftmost_array_bound_to_be_unspecified"></span><span id="ansi_c_only_allows_the_leftmost_array_bound_to_be_unspecified"></span><span id="ANSI_C_ONLY_ALLOWS_THE_LEFTMOST_ARRAY_BOUND_TO_BE_UNSPECIFIED"></span>ANSI C lässt nur zu, dass das am weitesten links gebundene Array nicht angegeben wird.</dt> <dd> In einem konformen Array lässt ANSI C zu, dass nur das äußerst linke (wichtigste) Array, das gebunden ist, nicht angegeben wird. Wenn mehrere Dimensionen konform sind, versucht MIDL, eine 1 in die anderen konformen &quot; &quot; Dimensionen zu setzen. Wenn die anderen Dimensionen in einer anderen Typdefinition definiert sind, ist dies nicht möglich. Versuchen Sie, alle Arraydimensionen in die Arraydeklaration zu setzen, um dies zu vermeiden. In jedem Fall sollten Sie vor den Vom Compiler durchgeführten Arrayindizierungsberechnungen vorsichtig sein. Möglicherweise müssen Sie ihre eigenen Berechnungen mit den tatsächlichen Größen durchführen.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2297"></span><span id="midl2297"></span><dl> <dt><strong>MIDL2297</strong></dt> </dl></td>
<td><dl> <dt><span id="by-value_union_parameters_not_supported_for__Oi_modes__using__Os"></span><span id="by-value_union_parameters_not_supported_for__oi_modes__using__os"></span><span id="BY-VALUE_UNION_PARAMETERS_NOT_SUPPORTED_FOR__OI_MODES__USING__OS"></span>By-Value-Union-Parameter werden für /Oi-Modi mit /Os nicht unterstützt.</dt> <dd> Diese Aktion wird für die vollständig interpretierte Optimierung nicht unterstützt. Wechsel zur Optimierung im gemischten Modus.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2298"></span><span id="midl2298"></span><dl> <dt><strong>MIDL2298</strong></dt> </dl></td>
<td><dl> <dt><span id="_version__attribute_is_ignored_on_an__object__interface"></span><span id="_VERSION__ATTRIBUTE_IS_IGNORED_ON_AN__OBJECT__INTERFACE"></span>[version]-Attribut wird auf einer [Object]-Schnittstelle ignoriert.</dt> <dd> Das Attribut [<a href="object.md"><strong>object</strong></a>] identifiziert eine COM-Schnittstelle. Eine Schnittstellenattributliste für eine COM-Schnittstelle darf nicht das Attribut [ <a href="version.md"><strong>version</strong></a>] enthalten.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2299"></span><span id="midl2299"></span><dl> <dt><strong>MIDL2299</strong></dt> </dl></td>
<td><dl> <dt><span id="_size_is__or__max_is__attribute_is_invalid_on_a_fixed_array"></span><span id="_SIZE_IS__OR__MAX_IS__ATTRIBUTE_IS_INVALID_ON_A_FIXED_ARRAY"></span>[size_is]- oder [max_is]-Attribut ist für ein festes Array ungültig.</dt> <dd> Arrays fester Größe können die Attribute size_is <a href="size-is.md"><strong>oder</strong></a> <a href="max-is.md"><strong>max_is</strong></a> nicht verwenden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2300"></span><span id="midl2300"></span><dl> <dt><strong>MIDL2300</strong></dt> </dl></td>
<td><dl> <dt><span id="_encode__or__decode__are_invalid_in_an__object__interface"></span><span id="_ENCODE__OR__DECODE__ARE_INVALID_IN_AN__OBJECT__INTERFACE"></span>[encode] oder [decode] sind in einer [Object]-Schnittstelle ungültig.</dt> <dd> Das Attribut [<a href="object.md"><strong>object</strong></a>] identifiziert eine COM-Schnittstelle. Die Attribute [<a href="encode.md"><strong>encode</strong></a>] und [ <a href="decode.md"><strong>decode</strong></a>] ermöglichen die Serialisierung. Das heißt, Sie können Puffer für das Datenmarshalling und das Unmarshal bereitstellen und steuern, aber Sie können keine Serialisierung für COM-Schnittstellen ausführen.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2301"></span><span id="midl2301"></span><dl> <dt><strong>MIDL2301</strong></dt> </dl></td>
<td><dl> <dt><span id="_encode__or__decode__on_a_type_requires__ms_ext"></span><span id="_ENCODE__OR__DECODE__ON_A_TYPE_REQUIRES__MS_EXT"></span>[encode] oder [decode] für einen Typ erfordert /ms_ext</dt> <dd> Die Serialisierung ist nicht Teil der DCE-IDL-Spezifikation. Es handelt sich um eine Microsoft-Erweiterung, die die Verwendung des Befehlszeilenschalters <a href="-ms-ext.md"><strong>/ms_ext</strong></a> erfordert.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2302"></span><span id="midl2302"></span><dl> <dt><strong>MIDL2302</strong></dt> </dl></td>
<td><dl> <dt><span id="int_not_supported_on__env_win16_or__env_dos"></span><span id="INT_NOT_SUPPORTED_ON__ENV_WIN16_OR__ENV_DOS"></span>int wird unter /env win16 oder /env dos nicht unterstützt.</dt> <dd> Die 16-Bit-Plattformen von Microsoft unterstützen die Verwendung des <a href="int.md"><strong>int-Typs</strong></a> in einer IDL-Datei nicht. Qualifizieren Sie <strong>den int-Typ</strong> <a href="small.md"><strong>mit small,</strong></a> <a href="short.md"><strong>short</strong></a>oder <a href="long.md"><strong>long.</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2303"></span><span id="midl2303"></span><dl> <dt><strong>MIDL2303</strong></dt> </dl></td>
<td><dl> <dt><span id="_bstring__may_only_be_applied_to_a_pointer_to__char__or__whchar_t_"></span><span id="_BSTRING__MAY_ONLY_BE_APPLIED_TO_A_POINTER_TO__CHAR__OR__WHCHAR_T_"></span>[bstring] darf nur auf einen Zeiger auf char oder &quot; whchar_t &quot; &quot;&quot;</dt> <dd> Dieser Fehler ist veraltet. Sie wird nur aus Gründen der Abwärtskompatibilität bereitgestellt.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2304"></span><span id="midl2304"></span><dl> <dt><strong>MIDL2304</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_invalid_on_a_procedure_in_an__object__interface"></span><span id="ATTRIBUTE_INVALID_ON_A_PROCEDURE_IN_AN__OBJECT__INTERFACE"></span>Für eine Prozedur in einer [Objekt]-Schnittstelle ungültiges Attribut</dt> <dd> Das angegebene Attribut ist für die Prozedur in einer COM-Schnittstelle nicht zulässig.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2305"></span><span id="midl2305"></span><dl> <dt><strong>MIDL2305</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_invalid_on_an__object__interface"></span><span id="ATTRIBUTE_INVALID_ON_AN__OBJECT__INTERFACE"></span>Attribut für eine [Objekt]-Schnittstelle ungültig</dt> <dd> Das angegebene Attribut ist in einer COM-Schnittstelle nicht zulässig.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2306"></span><span id="midl2306"></span><dl> <dt><strong>MIDL2306</strong></dt> </dl></td>
<td><dl> <dt><span id="too_many_parameters_or_stack_too_big_for__Oi_modes__using__Os"></span><span id="too_many_parameters_or_stack_too_big_for__oi_modes__using__os"></span><span id="TOO_MANY_PARAMETERS_OR_STACK_TOO_BIG_FOR__OI_MODES__USING__OS"></span>Zu viele Parameter oder stapeln zu groß für /Oi-Modi mit /Os</dt> <dd> Diese Warnung ist veraltet. Sie wird nur aus Gründen der Abwärtskompatibilität bereitgestellt. Gibt an, dass der Stapel durch den Aufruf der Remoteprozedur größer als 64 K wird.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2307"></span><span id="midl2307"></span><dl> <dt><strong>MIDL2307</strong></dt> </dl></td>
<td><dl> <dt><span id="no_attributes_on_ACF_file_typedef__so_no_effect"></span><span id="no_attributes_on_acf_file_typedef__so_no_effect"></span><span id="NO_ATTRIBUTES_ON_ACF_FILE_TYPEDEF__SO_NO_EFFECT"></span>keine Attribute in der ACF-Dateitypdefinition, daher hat dies keine Auswirkungen.</dt> <dd> Die IDL-Datei sollte alle typedef-Anweisungen enthalten, die keine Attribute haben. Sie sollten nicht in ACF-Dateien auftreten. Wenn sie dies tun, interpretiert der MIDL-Compiler sie als redundant und ignoriert sie.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2308"></span><span id="midl2308"></span><dl> <dt><strong>MIDL2308</strong></dt> </dl></td>
<td><dl> <dt><span id="calling_conventions_other_than___stdcall_or___cdecl_not_supported_for__Oi_modes__using__Os"></span><span id="calling_conventions_other_than___stdcall_or___cdecl_not_supported_for__oi_modes__using__os"></span><span id="CALLING_CONVENTIONS_OTHER_THAN___STDCALL_OR___CDECL_NOT_SUPPORTED_FOR__OI_MODES__USING__OS"></span>Andere Aufrufkonventionen als __stdcall oder __cdecl /Oi-Modi nicht unterstützt, mithilfe von /Os</dt> <dd> Aufrufkonventionen wie <strong>__pascal</strong> oder <strong>__fastcall</strong> ändern das Format des Stapels. Die <a href="-oi.md"><strong>/Oi-Modi</strong></a> unterstützen nur <strong>die</strong> __stdcall und <strong>__cdecl</strong> Aufrufkonventionen. Wenn Sie andere Aufrufkonventionen verwenden müssen, verwenden Sie den <a href="-os.md"><strong>Modus /Os.</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2309"></span><span id="midl2309"></span><dl> <dt><strong>MIDL2309</strong></dt> </dl></td>
<td><dl> <dt><span id="Too_many_delegation_methods_in_the_interface__require_Windows_2000_or_greater"></span><span id="too_many_delegation_methods_in_the_interface__require_windows_2000_or_greater"></span><span id="TOO_MANY_DELEGATION_METHODS_IN_THE_INTERFACE__REQUIRE_WINDOWS_2000_OR_GREATER"></span>Zu viele Delegierungsmethoden in der Schnittstelle erfordern Windows 2000 oder höher</dt> <dd> Eine Schnittstelle kann von einer anderen erben. In diesem Artikel werden die Methoden der Basisschnittstelle als delegiert betrachtet. Keine abgeleitete Schnittstelle kann mehr als 256 delegierte Methoden enthalten.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2310"></span><span id="midl2310"></span><dl> <dt><strong>MIDL2310</strong></dt> </dl></td>
<td><dl> <dt><span id="auto_handles_not_supported_with__env_mac_or__env_powermac"></span><span id="AUTO_HANDLES_NOT_SUPPORTED_WITH__ENV_MAC_OR__ENV_POWERMAC"></span>Automatische Handles, die mit /env mac oder /env powermac nicht unterstützt werden</dt> <dd> Beim Kompilieren der IDL-Datei für einen PowerMac können Sie keine automatischen Bindungshandles verwenden. Sie müssen explizite oder implizite Handles angeben.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2311"></span><span id="midl2311"></span><dl> <dt><strong>MIDL2311</strong></dt> </dl></td>
<td><dl> <dt><span id="statements_outside_library_block_are_illegal_in_mktyplib_compatibility_mode"></span><span id="STATEMENTS_OUTSIDE_LIBRARY_BLOCK_ARE_ILLEGAL_IN_MKTYPLIB_COMPATIBILITY_MODE"></span>Anweisungen außerhalb des Bibliotheksblocks sind im Mktyplib-Kompatibilitätsmodus unzulässig.</dt> <dd> Möglicherweise müssen Sie den Befehlszeilenschalter <a href="-mktyplib203.md"><strong>/mktyplib203</strong></a> angeben, wenn Sie Ihre IDL-Datei kompilieren.<br/>
<blockquote>
[!Note]<br />
Das Mktyplib.exe ist veraltet. Verwenden Sie stattdessen den MIDL-Compiler.
</blockquote>
<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2312"></span><span id="midl2312"></span><dl> <dt><strong>MIDL2312</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_syntax_unless_using_mktyplib_compatibility_mode"></span><span id="ILLEGAL_SYNTAX_UNLESS_USING_MKTYPLIB_COMPATIBILITY_MODE"></span>Ungültige Syntax, es sei denn, der Mktyplib-Kompatibilitätsmodus wird verwendet.</dt> <dd> Möglicherweise müssen Sie den Befehlszeilenschalter <a href="-mktyplib203.md"><strong>/mktyplib203</strong></a> angeben, wenn Sie Ihre IDL-Datei kompilieren.<br/>
<blockquote>
[!Note]<br />
Das Mktyplib.exe ist veraltet. Verwenden Sie stattdessen den MIDL-Compiler.
</blockquote>
<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2313"></span><span id="midl2313"></span><dl> <dt><strong>MIDL2313</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_definition__must_use_typedef_in_mktyplib_compatibility_mode"></span><span id="ILLEGAL_DEFINITION__MUST_USE_TYPEDEF_IN_MKTYPLIB_COMPATIBILITY_MODE"></span>Ungültige Definition, muss typedef im mktyplib-Kompatibilitätsmodus verwenden</dt> <dd> Möglicherweise müssen Sie den Befehlszeilenschalter <a href="-mktyplib203.md"><strong>/mktyplib203</strong></a> angeben, wenn Sie Ihre IDL-Datei kompilieren.<br/>
<blockquote>
[!Note]<br />
Das Mktyplib.exe ist veraltet. Verwenden Sie stattdessen den MIDL-Compiler.
</blockquote>
<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2314"></span><span id="midl2314"></span><dl> <dt><strong>MIDL2314</strong></dt> </dl></td>
<td><dl> <dt><span id="explicit_pointer_attribute__ptr___ref__ignored_for_interface_pointers"></span><span id="EXPLICIT_POINTER_ATTRIBUTE__PTR___REF__IGNORED_FOR_INTERFACE_POINTERS"></span>Explizites Zeigerattribut [ptr] [ref] für Schnittstellenzeiger ignoriert</dt> <dd> Zeiger auf Schnittstellen dürfen keine IDL-Attribute aufweisen.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2315"></span><span id="midl2315"></span><dl> <dt><strong>MIDL2315</strong></dt> </dl></td>
<td><a href="-oi.md"><strong>/Oi-Modi</strong></a> nicht für PowerMac implementiert, Wechsel zu <a href="-os.md"> <strong>/Os</strong></a><br/></td>
</tr>
<tr class="odd">
<td><span id="MIDL2316"></span><span id="midl2316"></span><dl> <dt><strong>MIDL2316</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_expression_type_used_in_attribute"></span><span id="ILLEGAL_EXPRESSION_TYPE_USED_IN_ATTRIBUTE"></span>Ungültiger Ausdruckstyp, der im Attribut verwendet wird</dt> <dd> Der Standardwert für den Zeiger sollte eine Konstante sein.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2317"></span><span id="midl2317"></span><dl> <dt><strong>MIDL2317</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_type_used_in_pipe"></span><span id="ILLEGAL_TYPE_USED_IN_PIPE"></span>Ungültiger Typ, der in pipe verwendet wird</dt> <dd> Pipes sind auf grundlegende IDL-Datentypen beschränkt. Beispielsweise können Sie keine Pipe von Arrays angeben.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2318"></span><span id="midl2318"></span><dl> <dt><strong>MIDL2318</strong></dt> </dl></td>
<td><dl> <dt><span id="procedure_uses_pipes__using__Oicf"></span><span id="procedure_uses_pipes__using__oicf"></span><span id="PROCEDURE_USES_PIPES__USING__OICF"></span>-Prozedur verwendet Pipes mit /Oicf</dt> <dd> Der ausgewählte Modus unterstützt keine Pipes. Der MIDL-Compiler hat die Verwendung von einem oder mehreren Pipes in ihrer Schnittstelle erkannt. Daher wird die IDL-Datei im <a href="-oi.md"><strong>/Oicf-Modus</strong></a> kompiliert.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2319"></span><span id="midl2319"></span><dl> <dt><strong>MIDL2319</strong></dt> </dl></td>
<td><dl> <dt><span id="procedure_has_an_attribute_that_requires_use_of__Oif__switching_modes"></span><span id="procedure_has_an_attribute_that_requires_use_of__oif__switching_modes"></span><span id="PROCEDURE_HAS_AN_ATTRIBUTE_THAT_REQUIRES_USE_OF__OIF__SWITCHING_MODES"></span>Prozedur verfügt über ein Attribut, das die Verwendung von /Oif erfordert, Umschaltmodi</dt> <dd> Sie müssen<a href="async.md"><strong>[asynchrone]</strong></a>Prozeduren im <a href="-oi.md"><strong>/Oif-Modus</strong></a> kompilieren.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2320"></span><span id="midl2320"></span><dl> <dt><strong>MIDL2320</strong></dt> </dl></td>
<td><dl> <dt><span id="conflicting_optimization_requirements__cannot_optimize"></span><span id="CONFLICTING_OPTIMIZATION_REQUIREMENTS__CANNOT_OPTIMIZE"></span>Widersprüchliche Optimierungsanforderungen, kann nicht optimiert werden</dt> <dd> Dieser Fehler weist häufig darauf hin, dass Sie sowohl <a href="-os.md"><strong>/Os</strong></a> als auch <a href="-oi.md"><strong>/Oi</strong></a> (oder eine Variante von <strong>/Oi</strong>) MIDL-Compilermodi angegeben haben. Dies kann auch bedeuten, dass die Funktionen, die Sie in Ihren IDL- und ACL-Dateien angegeben haben, beide Modi erfordern. Sie müssen den einen oder den anderen Modus auswählen, um die Optimierung durchzuführen.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2321"></span><span id="midl2321"></span><dl> <dt><strong>MIDL2321</strong></dt> </dl></td>
<td><dl> <dt><span id="pipes_cannot_be_array_elements__or_members_of_structures_or_unions"></span><span id="PIPES_CANNOT_BE_ARRAY_ELEMENTS__OR_MEMBERS_OF_STRUCTURES_OR_UNIONS"></span>Pipes können keine Arrayelemente oder Member von Strukturen oder Unions sein.</dt> <dd> Pipe-Datentypen können nur Parameter der obersten Ebene sein.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2322"></span><span id="midl2322"></span><dl> <dt><strong>MIDL2322</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid_pipe_usage"></span><span id="INVALID_PIPE_USAGE"></span>Ungültige Pipeverwendung</dt> <dd> Sie können Pipes nicht mit den Attributen [<a href="transmit-as.md"><strong>transmit_as</strong></a>], [<a href="represent-as.md"><strong>represent_as</strong></a>] oder [<a href="user-marshal.md"><strong>user_marshal</strong></a>] verwenden. Darüber hinaus können Pipes nicht als Rückgabetypen verwendet werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2323"></span><span id="midl2323"></span><dl> <dt><strong>MIDL2323</strong></dt> </dl></td>
<td><dl> <dt><span id="feature_requires_the_advanced_interpreted_optimization_option__use_-Oicf"></span><span id="feature_requires_the_advanced_interpreted_optimization_option__use_-oicf"></span><span id="FEATURE_REQUIRES_THE_ADVANCED_INTERPRETED_OPTIMIZATION_OPTION__USE_-OICF"></span>-Feature erfordert die erweiterte interpretierte Optimierungsoption. Verwenden von -Oicf</dt> <dd> Dieser Fehler weist darauf hin, dass MIDL-Compilerbefehlszeilenschalter wie <a href="-robust.md"><strong>/robust</strong></a> die Verwendung des <a href="-oi.md"><strong>/Oicf-Modus</strong></a> erfordern.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2324"></span><span id="midl2324"></span><dl> <dt><strong>MIDL2324</strong></dt> </dl></td>
<td><dl> <dt><span id="feature_requires_the_advanced_interpreted_optimization_option__use_-Oicf"></span><span id="feature_requires_the_advanced_interpreted_optimization_option__use_-oicf"></span><span id="FEATURE_REQUIRES_THE_ADVANCED_INTERPRETED_OPTIMIZATION_OPTION__USE_-OICF"></span>-Feature erfordert die erweiterte interpretierte Optimierungsoption. Verwenden von -Oicf</dt> <dd> Diese Warnung weist darauf hin, dass MIDL-Compilerbefehlszeilenschalter wie <a href="-robust.md"><strong>/robust</strong></a> die Verwendung des <a href="-oi.md"><strong>/Oicf-Modus</strong></a> erfordern.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2329"></span><span id="midl2329"></span><dl> <dt><strong>MIDL2329</strong></dt> </dl></td>
<td><dl> <dt><span id="the_optimization_option_is_being_phased_out__use_-Oic"></span><span id="the_optimization_option_is_being_phased_out__use_-oic"></span><span id="THE_OPTIMIZATION_OPTION_IS_BEING_PHASED_OUT__USE_-OIC"></span>Die Optimierungsoption wird eingestellt, verwenden Sie -Oic.</dt> <dd> Der <a href="-oi.md"><strong>Optimierungsmodus /Oi1</strong></a> wurde in der MIDL-Befehlszeile angegeben. Dieser Modus wird nicht mehr unterstützt, und stattdessen sollte <strong>/Oicf</strong> verwendet werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2330"></span><span id="midl2330"></span><dl> <dt><strong>MIDL2330</strong></dt> </dl></td>
<td><dl> <dt><span id="the_optimization_option_is_being_phased_out__use_-Oicf"></span><span id="the_optimization_option_is_being_phased_out__use_-oicf"></span><span id="THE_OPTIMIZATION_OPTION_IS_BEING_PHASED_OUT__USE_-OICF"></span>Die Optimierungsoption wird eingestellt, verwenden Sie -Oicf.</dt> <dd> Der <a href="-oi.md"><strong>Optimierungsmodus /Oi2</strong></a> wurde in der MIDL-Befehlszeile angegeben. Dieser Modus wird nicht mehr unterstützt, und stattdessen sollte <strong>/Oicf</strong> verwendet werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2331"></span><span id="midl2331"></span><dl> <dt><strong>MIDL2331</strong></dt> </dl></td>
<td><dl> <dt><span id="the_optimization_option_is_being_phased_out__use_-ic"></span><span id="THE_OPTIMIZATION_OPTION_IS_BEING_PHASED_OUT__USE_-IC"></span>Die Optimierungsoption wird eingestellt, verwenden Sie -ic.</dt> <dd> Der i1-Optimierungsmodus wurde in einem [optimize]-ACF-Attribut angegeben. Dieser Modus wird nicht mehr unterstützt, und stattdessen sollte icf verwendet werden.<br/> ACF-Beispieldatei:<br/>
<pre class="syntax" data-space="preserve"><code>[optimize(&quot;i1&quot;)] roo();    //MIDL 2331</code></pre>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2332"></span><span id="midl2332"></span><dl> <dt><strong>MIDL2332</strong></dt> </dl></td>
<td><dl> <dt><span id="the_optimization_option_is_being_phased_out__use_-icf"></span><span id="THE_OPTIMIZATION_OPTION_IS_BEING_PHASED_OUT__USE_-ICF"></span>Die Optimierungsoption wird eingestellt, verwenden Sie -icf.</dt> <dd> Der i2-Optimierungsmodus wurde in einem [optimize]-ACF-Attribut angegeben. Dieser Modus wird nicht mehr unterstützt, und stattdessen sollte icf verwendet werden.<br/> ACF-Beispieldatei:<br/>
<pre class="syntax" data-space="preserve"><code>[optimize(&quot;i2&quot;)] roo();    //MIDL 2332</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2333"></span><span id="midl2333"></span><dl> <dt><strong>MIDL2333</strong></dt> </dl></td>
<td><dl> <dt><span id="the_-old_and_-new_switches_are_obsolete__use_-oldtlb_and_-newtlb"></span><span id="THE_-OLD_AND_-NEW_SWITCHES_ARE_OBSOLETE__USE_-OLDTLB_AND_-NEWTLB"></span>Die Schalter "-old" und "-new" sind veraltet. Verwenden Sie "-oldtlb" und "-newtlb".</dt> <dd> Diese Meldung ist veraltet und wird von MIDL nicht mehr ausgelassen.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2334"></span><span id="midl2334"></span><dl> <dt><strong>MIDL2334</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_argument_value"></span><span id="ILLEGAL_ARGUMENT_VALUE"></span>Ungültiger Argumentwert</dt> <dd> Zu den zulässigen Varianten des /O-Befehlszeilenschalters gehören <a href="-os.md"><strong>/Os,</strong></a> <a href="-oi.md"><strong>/Oi,</strong></a> <strong>/Oic,</strong> <strong>/Oicf</strong>und <strong>/Oif.</strong><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2335"></span><span id="midl2335"></span><dl> <dt><strong>MIDL2335</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_expression_type_in_constant"></span><span id="ILLEGAL_EXPRESSION_TYPE_IN_CONSTANT"></span>Ungültiger Ausdruckstyp in Konstanten</dt> <dd> Der Ausdruck wird nicht zu einer Konstante ausgewertet.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2336"></span><span id="midl2336"></span><dl> <dt><strong>MIDL2336</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_expression_type_in_enum"></span><span id="ILLEGAL_EXPRESSION_TYPE_IN_ENUM"></span>Ungültiger Ausdruckstyp in Enumeration</dt> <dd> Ein aufzählter Wert in einer <a href="enum.md"><strong>Enumerationsdefinition</strong></a> wird nicht zu einem ganzzahligen Typ ausgewertet.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2337"></span><span id="midl2337"></span><dl> <dt><strong>MIDL2337</strong></dt> </dl></td>
<td><dl> <dt><span id="unsatisfied_forward_declaration"></span><span id="UNSATISFIED_FORWARD_DECLARATION"></span>Nicht erfüllte Vorwärtsdeklaration</dt> <dd> Der MIDL-Compiler konnte die Definition einer Vorwärtsdeklaration nicht auflösen.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2338"></span><span id="midl2338"></span><dl> <dt><strong>MIDL2338</strong></dt> </dl></td>
<td><dl> <dt><span id="switches_are_contradictory"></span><span id="SWITCHES_ARE_CONTRADICTORY"></span>Schalter sind unerzwend</dt> <dd> Sie können die Befehlszeilenschalter <a href="-osf.md"><strong>/osf</strong></a> und <a href="-ms-ext.md"><strong>/ms_ext</strong></a> nicht verwenden, wenn Sie eine IDL-Datei kompilieren. Sie müssen das eine oder das andere auswählen.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2339"></span><span id="midl2339"></span><dl> <dt><strong>MIDL2339</strong></dt> </dl></td>
<td><dl> <dt><span id="MIDL_cannot_generate_HOOKOLE_information_for_the_non-rpc-able_union"></span><span id="midl_cannot_generate_hookole_information_for_the_non-rpc-able_union"></span><span id="MIDL_CANNOT_GENERATE_HOOKOLE_INFORMATION_FOR_THE_NON-RPC-ABLE_UNION"></span>MIDL kann keine HOOKOLE-Informationen für die Nicht-RPC-fähige Union generieren.</dt> <dd> Dieser Fehler ist veraltet. Sie wird ausschließlich aus Gründen der Abwärtskompatibilität bereitgestellt.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2340"></span><span id="midl2340"></span><dl> <dt><strong>MIDL2340</strong></dt> </dl></td>
<td><dl> <dt><span id="no_case_expression_found_for_union"></span><span id="NO_CASE_EXPRESSION_FOUND_FOR_UNION"></span>Für union wurde kein Case-Ausdruck gefunden.</dt> <dd> Jedes Feld einer Union muss über eine case-Anweisung mit einem konstanten Ausdruck verfügen.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2341"></span><span id="midl2341"></span><dl> <dt><strong>MIDL2341</strong></dt> </dl></td>
<td><dl> <dt><span id="_user_marshal__and__wire_marshal__not_supported_with_-Oi_and_-Oic_flags__use_-Os_or_-Oicf"></span><span id="_user_marshal__and__wire_marshal__not_supported_with_-oi_and_-oic_flags__use_-os_or_-oicf"></span><span id="_USER_MARSHAL__AND__WIRE_MARSHAL__NOT_SUPPORTED_WITH_-OI_AND_-OIC_FLAGS__USE_-OS_OR_-OICF"></span>[user_marshal] und [wire_marshal] werden mit den Flags -Oi und -Oic nicht unterstützt. Verwenden Sie -Os oder -Oicf.</dt> <dd> Die Attribute [<a href="user-marshal.md"><strong>user_marshal</strong></a>] und [<a href="wire-marshal.md"><strong>wire_marshal</strong></a>] erfordern die spezifischen Optimierungsfeatures, die nur in <a href="-oi.md"><strong>/Oicf</strong></a> (codeloser Proxy mit schnellen Formatzeichenfolgen) oder <a href="-os.md"><strong>/Os</strong></a> (Marshalling im gemischten Modus) verfügbar sind.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2342"></span><span id="midl2342"></span><dl> <dt><strong>MIDL2342</strong></dt> </dl></td>
<td><dl> <dt><span id="pipes_can_t_be_used_with_data_serialization__i.e.__encode__and_or__decode_"></span><span id="PIPES_CAN_T_BE_USED_WITH_DATA_SERIALIZATION__I.E.__ENCODE__AND_OR__DECODE_"></span>Pipes können nicht bei der Datenserialisierung verwendet werden, d. h. [Codierung] und/oder [Decodierung]</dt> <dd> Sie können Pipes nicht als Parameter an Prozeduren übergeben, die über die Attribute [<a href="encode.md"><strong>encode</strong></a>] oder [<a href="decode.md"><strong>decode</strong></a>] verfügen.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2343"></span><span id="midl2343"></span><dl> <dt><strong>MIDL2343</strong></dt> </dl></td>
<td><dl> <dt><span id="all_pipe_interface_pointers_must_use_single_indirection"></span><span id="ALL_PIPE_INTERFACE_POINTERS_MUST_USE_SINGLE_INDIRECTION"></span>Alle Pipeschnittstellenzeiger müssen eine einzelne Dekonstruktion verwenden.</dt> <dd> Sie können auf diese Weise keinen Zeiger auf einen Zeiger auf eine Pipeschnittstelle verwenden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2344"></span><span id="midl2344"></span><dl> <dt><strong>MIDL2344</strong></dt> </dl></td>
<td><dl> <dt><span id="_iid_is____cannot_be_used_with_a_pipe_interface_pointer"></span><span id="_IID_IS____CANNOT_BE_USED_WITH_A_PIPE_INTERFACE_POINTER"></span>[iid_is()] kann nicht mit einem Pipeschnittstellenzeiger verwendet werden.</dt> <dd> Diese Meldung ist veraltet. Diese Meldung wird vom Compiler nicht mehr verwendet.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2345"></span><span id="midl2345"></span><dl> <dt><strong>MIDL2345</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid_or_inapplicable_-lcid_switch"></span><span id="INVALID_OR_INAPPLICABLE_-LCID_SWITCH"></span>Ungültiger oder nicht gültiger Schalter "-lcid"</dt> <dd> Der von Ihnen angegebene lokale Bezeichner (LCID) ist ungültig.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2346"></span><span id="midl2346"></span><dl> <dt><strong>MIDL2346</strong></dt> </dl></td>
<td><dl> <dt><span id="the_specified_lcid_is_different_from_previous_specification"></span><span id="THE_SPECIFIED_LCID_IS_DIFFERENT_FROM_PREVIOUS_SPECIFICATION"></span>Die angegebene LCID unterscheidet sich von der vorherigen Spezifikation.</dt> <dd> Die in /lcid und [<a href="lcid.md"><strong>lcid</strong></a>] angegebenen Werte unterscheiden sich. Der MIDL-Compiler verwendet den letzten definierten.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2347"></span><span id="midl2347"></span><dl> <dt><strong>MIDL2347</strong></dt> </dl></td>
<td><dl> <dt><span id="importlib_is_not_allowed_outside_of_a_library_block"></span><span id="IMPORTLIB_IS_NOT_ALLOWED_OUTSIDE_OF_A_LIBRARY_BLOCK"></span>importlib ist außerhalb eines Bibliotheksblocks nicht zulässig.</dt> <dd> Alle<a href="importlib.md"><strong>[importlib]-Anweisungen</strong></a>sollten in einem<a href="library.md"><strong>[Library]-Block</strong></a>auftreten.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2348"></span><span id="midl2348"></span><dl> <dt><strong>MIDL2348</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid_floating_point_value"></span><span id="INVALID_FLOATING_POINT_VALUE"></span>Ungültiger Gleitkommawert</dt> <dd> Dieser Fehler sollte nicht von MIDL ausgegeben werden. Wenn dieser Fehler angezeigt wird, melden Sie einen Fehler an Microsoft, der alle Dateien bereitstellt, die zum Reproduzieren des Fehlers erforderlich sind, einschließlich Ihrer IDL-Dateien, ACF-Dateien, Header usw.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2349"></span><span id="midl2349"></span><dl> <dt><strong>MIDL2349</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid_member"></span><span id="INVALID_MEMBER"></span>Ungültiger Member</dt> <dd> Prozeduren können keine Member einer Bibliothek sein.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2350"></span><span id="midl2350"></span><dl> <dt><strong>MIDL2350</strong></dt> </dl></td>
<td><dl> <dt><span id="possible_invalid_member"></span><span id="POSSIBLE_INVALID_MEMBER"></span>Möglicherweise ungültiger Member</dt> <dd> Um ein gültiger Member einer Bibliothek zu sein, muss das Bibliothekselement ein Modul, eine Disp-Schnittstelle, eine Co-Klasse, eine if-Anweisung, eine Struktur, eine Union, eine Enumeration oder eine Vorwärtsdeklaration sein.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2351"></span><span id="midl2351"></span><dl> <dt><strong>MIDL2351</strong></dt> </dl></td>
<td><dl> <dt><span id="mismatch_in_pipe_and_interface_types"></span><span id="MISMATCH_IN_PIPE_AND_INTERFACE_TYPES"></span>Nichtübereinstimmung in Pipe- und Schnittstellentypen</dt> <dd> Diese Meldung ist veraltet.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2352"></span><span id="midl2352"></span><dl> <dt><strong>MIDL2352</strong></dt> </dl></td>
<td><dl> <dt><span id="string__varying_array__conformant_array_and_full_pointer_parameters_may_be_incompatible_with_pipe_parameters_during_run_time"></span><span id="STRING__VARYING_ARRAY__CONFORMANT_ARRAY_AND_FULL_POINTER_PARAMETERS_MAY_BE_INCOMPATIBLE_WITH_PIPE_PARAMETERS_DURING_RUN_TIME"></span>Zeichenfolgen-, variierende Array-, konforme Array- und vollständige Zeigerparameter können während der Laufzeit nicht mit Pipeparametern kompatibel sein.</dt> <dd> Eine Methode, die eine oder mehrere [in]-Zeichenfolgen, unterschiedliche Arrays, konforme Arrays und vollständige Zeigerparameter und alle [in]-Pipeparameter kombiniert, führt zur Generierung eines Stubs, der nur auf <strong>ncacn_*</strong> und <a href="ncalrpc.md"><strong>ncalrpc-Protokollsequenzen</strong></a> auf Windows Computern ausgeführt wird. Wenn Sie den Stub verwenden, um Aufrufe für <strong>ncadg_*-Protokollsequenzen</strong> auszuführen oder Aufrufe von anderen OSF-DCE-RPC-Anbietern zu akzeptieren, können während der Laufzeit Fehler auf dem Server generiert werden. Dieser Fehler tritt ab Windows Server 2003 auf.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2353"></span><span id="midl2353"></span><dl> <dt><strong>MIDL2353</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_must_be_in"></span><span id="PARAMETER_MUST_BE_IN"></span>-Parameter muss sich in</dt> <dd> Asynchrone Handles müssen<a href="in.md"><strong>[in</strong></a>]-Parametern sein.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2354"></span><span id="midl2354"></span><dl> <dt><strong>MIDL2354</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_type_of_an__async__object_must_be_a_double_pointer_to_an_interface"></span><span id="PARAMETER_TYPE_OF_AN__ASYNC__OBJECT_MUST_BE_A_DOUBLE_POINTER_TO_AN_INTERFACE"></span>Der Parametertyp eines [async]-Objekts muss ein doppelter Zeiger auf eine Schnittstelle sein.</dt> <dd> Der Parameter muss vom Typ <strong>IAsyncManager</strong> ** sein.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2355"></span><span id="midl2355"></span><dl> <dt><strong>MIDL2355</strong></dt> </dl></td>
<td><dl> <dt><span id="incorrect_async_handle_type"></span><span id="INCORRECT_ASYNC_HANDLE_TYPE"></span>Falscher asynchroner Handletyp</dt> <dd> Der Handletyp sollte <strong>IAsyncManager</strong> oder ein von <strong>IAsyncManager</strong>abgeleiteter Typ sein.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2356"></span><span id="midl2356"></span><dl> <dt><strong>MIDL2356</strong></dt> </dl></td>
<td><dl> <dt><span id="the__internal__switch_enables_unsupported_features__use_with_caution"></span><span id="THE__INTERNAL__SWITCH_ENABLES_UNSUPPORTED_FEATURES__USE_WITH_CAUTION"></span>Der &quot; interne Switch aktiviert nicht unterstützte &quot; Features, verwenden Sie mit Vorsicht.</dt> <dd> Vermeiden Sie die Verwendung dieses Schalters.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2357"></span><span id="midl2357"></span><dl> <dt><strong>MIDL2357</strong></dt> </dl></td>
<td><dl> <dt><span id="async_procedures_cannot_use_auto_handle"></span><span id="ASYNC_PROCEDURES_CANNOT_USE_AUTO_HANDLE"></span>Asynchrone Prozeduren können kein automatisches Handle verwenden</dt> <dd> Prozeduren mit dem Attribut [<a href="async.md"><strong>async</strong></a>] erfordern explizite Handles.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2358"></span><span id="midl2358"></span><dl> <dt><strong>MIDL2358</strong></dt> </dl></td>
<td><dl> <dt><span id="error_status_t_should_have_both__comm_status__and__fault_status_"></span><span id="ERROR_STATUS_T_SHOULD_HAVE_BOTH__COMM_STATUS__AND__FAULT_STATUS_"></span>error_status_t sollten über [comm_status] und [fault_status] verfügen.</dt> <dd> Eine Prozedur wurde mit den IDL-Attributen [maybe] oder [message] angegeben, aber der Rückgabetyp verfügt nur über die ACF-Attribute [comm_status] oder [fault_status]. Beide ACF-Attribute sind erforderlich.<br/> ACF-Beispieldatei:<br/>
<pre class="syntax" data-space="preserve"><code>[comm_status] roo();    //MIDL 2358
[fault_status] bar();    //MIDL 2358
[comm_status, fault_status] baz();    //OK</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2359"></span><span id="midl2359"></span><dl> <dt><strong>MIDL2359</strong></dt> </dl></td>
<td><dl> <dt><span id="this_construct_is_only_allowed_within_a_library_block"></span><span id="THIS_CONSTRUCT_IS_ONLY_ALLOWED_WITHIN_A_LIBRARY_BLOCK"></span>Dieses Konstrukt ist nur innerhalb eines Bibliotheksblocks zulässig.</dt> <dd> Ein Modul kann nur innerhalb eines Bibliotheksblocks auftreten.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2360"></span><span id="midl2360"></span><dl> <dt><strong>MIDL2360</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid_type_redefinition"></span><span id="INVALID_TYPE_REDEFINITION"></span>Ungültige Typdefinition</dt> <dd> Ein neuer Typ wurde rekursiv für einen nicht vorhandenen Typ definiert.<br/> Beispiel:<br/>
<pre class="syntax" data-space="preserve"><code>typedef roo roo[10];    //MIDL 2360</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2361"></span><span id="midl2361"></span><dl> <dt><strong>MIDL2361</strong></dt> </dl></td>
<td><dl> <dt><span id="procedures_with_a__vararg__attribute_must_have_a_SAFEARRAY_VARIANT__parameter__param_order_is__vararg____lcid____retval_"></span><span id="procedures_with_a__vararg__attribute_must_have_a_safearray_variant__parameter__param_order_is__vararg____lcid____retval_"></span><span id="PROCEDURES_WITH_A__VARARG__ATTRIBUTE_MUST_HAVE_A_SAFEARRAY_VARIANT__PARAMETER__PARAM_ORDER_IS__VARARG____LCID____RETVAL_"></span>Prozeduren mit einem [lvarg]-Attribut müssen über einen SAFEARRAY(VARIANT)-Parameter verfügen. param order is [lvarg], [lcid], [retval]</dt> <dd> Die meisten Parameter für Prozeduren mit dem<a href="vararg.md"><strong>[lvarg</strong></a>]-Attribut müssen vor dem <strong>SAFEARRAY(VARIANT)-Parameter</strong> auftreten. Der <strong>SAFEARRAY(VARIANT)-Parameter</strong> muss vorhanden sein. Wenn die Parameterliste einen Parameter mit dem Attribut [ <a href="lcid.md"><strong>lcid</strong></a>] enthält, muss sie dem <strong>PARAMETER SAFEARRAY(VARIANT)</strong> folgen. Wenn die Parameterliste einen Parameter mit dem Attribut [<a href="retval.md"><strong>retval</strong></a>] enthält, muss sie nach dem Parameter mit dem Attribut [<strong>lcid</strong>] auftreten.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2363"></span><span id="midl2363"></span><dl> <dt><strong>MIDL2363</strong></dt> </dl></td>
<td><dl> <dt><span id="too_many_methods_in_the_interface__requires_Windows_2000_or_greater"></span><span id="too_many_methods_in_the_interface__requires_windows_2000_or_greater"></span><span id="TOO_MANY_METHODS_IN_THE_INTERFACE__REQUIRES_WINDOWS_2000_OR_GREATER"></span>zu viele Methoden in der -Schnittstelle, erfordert Windows 2000 oder höher</dt> <dd> Der MIDL-Compiler lässt beim Kompilieren im <a href="-oi.md"><strong>/Oicf-Modus</strong></a> nicht mehr als 1024 Methoden in einer Schnittstelle zu.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2364"></span><span id="midl2364"></span><dl> <dt><strong>MIDL2364</strong></dt> </dl></td>
<td><dl> <dt><span id="switch_is_being_phased_out"></span><span id="SWITCH_IS_BEING_PHASED_OUT"></span>Switch wird eingestellt</dt> <dd> Die folgenden Schalter sind veraltet: /<strong>hookole</strong>, /<strong>env win16</strong>und /<strong>env</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2365"></span><span id="midl2365"></span><dl> <dt><strong>MIDL2365</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_derive_from_IAdviseSink__IAdviseSink2__or_IAdviseSinkEx"></span><span id="cannot_derive_from_iadvisesink__iadvisesink2__or_iadvisesinkex"></span><span id="CANNOT_DERIVE_FROM_IADVISESINK__IADVISESINK2__OR_IADVISESINKEX"></span>kann nicht von IAdviseSink, IAdviseSink2 oder IAdviseSinkEx abgeleitet werden.</dt> <dd> Diese Schnittstellen können nicht erweitert werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2366"></span><span id="midl2366"></span><dl> <dt><strong>MIDL2366</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_assign_a_default_value"></span><span id="CANNOT_ASSIGN_A_DEFAULT_VALUE"></span>kann keinen Standardwert zuweisen.</dt> <dd> Das Zuweisen eines Standardwerts zu einem Parameter ist in Visual Basic zulässig, aber nicht in C++. Wenn Sie C++ verwenden, wird der Standardwert ignoriert.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2367"></span><span id="midl2367"></span><dl> <dt><strong>MIDL2367</strong></dt> </dl></td>
<td><dl> <dt><span id="type_library_generation_for_DOS_Win16_MAC_is_not_supported"></span><span id="type_library_generation_for_dos_win16_mac_is_not_supported"></span><span id="TYPE_LIBRARY_GENERATION_FOR_DOS_WIN16_MAC_IS_NOT_SUPPORTED"></span>Die Generierung der Typbibliothek für DOS/Win16/MAC wird nicht unterstützt.</dt> <dd> MIDL unterstützt keine 16-Bit-Typbibliotheken.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2368"></span><span id="midl2368"></span><dl> <dt><strong>MIDL2368</strong></dt> </dl></td>
<td><dl> <dt><span id="error_generating_type_library__ignored"></span><span id="ERROR_GENERATING_TYPE_LIBRARY__IGNORED"></span>Fehler beim Generieren der Typbibliothek, ignoriert</dt> <dd> Beim Generieren der Typbibliothek ist ein nicht schwerwiegender Fehler aufgetreten.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2369"></span><span id="midl2369"></span><dl> <dt><strong>MIDL2369</strong></dt> </dl></td>
<td><dl> <dt><span id="exceeded_stack_size_for__Oi__using__Os"></span><span id="exceeded_stack_size_for__oi__using__os"></span><span id="EXCEEDED_STACK_SIZE_FOR__OI__USING__OS"></span>Überschrittene Stapelgröße für /Oi mit /Os</dt> <dd> Der Optimierungsmodus -Oi ist auf 128 Bytes Stapelspeicherplatz für Parameter beschränkt. Der Compiler hat automatisch in den Betriebssystemoptimierungsmodus gewechselt, um diese Einschränkung zu umgehen.<br/> Um diese Warnung zu vermeiden, verwenden Sie die Optimierungsmodi -Oicf oder -Os. Der Optimierungsmodus kann in der Befehlszeile geändert werden, indem -Oicf oder -Os anstelle von -Oi angegeben oder der Funktion in der ACF-Datei ein [optimize9 &quot; icf &quot; )]- oder optimize[(s &quot; &quot; )]-Attribut hinzugefügt wird.<br/> Diese Warnung tritt in der Regel auf, wenn große Strukturen als Parameter nach Wert übergeben werden. Die erforderliche Stapelgröße kann verringert werden, indem stattdessen ein Zeiger auf die -Struktur übergeben wird.<br/> Beispiel:<br/>
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
<td><dl> <dt><span id="use_of__robust_requires__Oicf__switching_modes"></span><span id="use_of__robust_requires__oicf__switching_modes"></span><span id="USE_OF__ROBUST_REQUIRES__OICF__SWITCHING_MODES"></span>Die Verwendung von /robust erfordert /Oicf, Wechselmodi</dt> <dd> Sie müssen im <a href="-oi.md"><strong>/Oicf-Modus</strong></a> kompilieren, wenn Sie den Schalter <a href="-robust.md"><strong>/robust</strong></a> in der Befehlszeile angeben.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2371"></span><span id="midl2371"></span><dl> <dt><strong>MIDL2371</strong></dt> </dl></td>
<td><dl> <dt><span id="incorrect_range_specified"></span><span id="INCORRECT_RANGE_SPECIFIED"></span>Falscher bereich angegeben</dt> <dd> Der höchste wert, der in einem<a href="range.md"><strong>[range]-Attribut</strong></a>angegeben ist, ist kleiner als der niedrigste Wert.<br/> Beispiel:<br/>
<pre class="syntax" data-space="preserve"><code>void roo([range(3,2)] int a);    //MIDL 2371</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2372"></span><span id="midl2372"></span><dl> <dt><strong>MIDL2372</strong></dt> </dl></td>
<td><dl> <dt><span id="_invalid_combination_of__in__only_and__out__parameters_for__async_uuid__interface"></span><span id="_INVALID_COMBINATION_OF__IN__ONLY_AND__OUT__PARAMETERS_FOR__ASYNC_UUID__INTERFACE"></span> Ungültige Kombination der [in]-Parameter und [out]-Parameter für die [async_uuid]-Schnittstelle</dt> <dd> Für diesen Schnittstellentyp sind nur einfache Kombinationen von Attributen mit<a href="in.md"><strong>[in]-</strong></a>oder<a href="out-idl.md"><strong>[out]-Parametern</strong></a>zulässig.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2373"></span><span id="midl2373"></span><dl> <dt><strong>MIDL2373</strong></dt> </dl></td>
<td><dl> <dt><span id="DOS__Win16_and_MAC_platforms_are_not_supported_with__robust"></span><span id="dos__win16_and_mac_platforms_are_not_supported_with__robust"></span><span id="DOS__WIN16_AND_MAC_PLATFORMS_ARE_NOT_SUPPORTED_WITH__ROBUST"></span>DOS-, Win16- und MAC-Plattformen werden mit /robust nicht unterstützt.</dt> <dd> MIDL unterstützt den Schalter <a href="-robust.md"><strong>/robust</strong></a> auf Microsoft Windows 2000 oder höher.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2374"></span><span id="midl2374"></span><dl> <dt><strong>MIDL2374</strong></dt> </dl></td>
<td><dl> <dt><span id="support_for_NT_3.51_style_stubless_proxies_for_object_interfaces_will_be_phased_out__use__Oif."></span><span id="support_for_nt_3.51_style_stubless_proxies_for_object_interfaces_will_be_phased_out__use__oif."></span><span id="SUPPORT_FOR_NT_3.51_STYLE_STUBLESS_PROXIES_FOR_OBJECT_INTERFACES_WILL_BE_PHASED_OUT__USE__OIF."></span>Unterstützung für Stublose Proxys im NT 3.51-Format für Objektschnittstellen wird eingestellt. verwenden Sie /Oif.</dt> <dd> Dieser Modus ist veraltet. Verwenden Sie <a href="-oi.md"><strong>/Oif</strong></a> oder <strong>/Oicf.</strong><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2375"></span><span id="midl2375"></span><dl> <dt><strong>MIDL2375</strong></dt> </dl></td>
<td><dl> <dt><span id="_encode__or__decode__with__robust_requires__Oicf"></span><span id="_encode__or__decode__with__robust_requires__oicf"></span><span id="_ENCODE__OR__DECODE__WITH__ROBUST_REQUIRES__OICF"></span>[encode] oder [decode] mit /robust erfordert /Oicf</dt> <dd> Die Serialisierung kann nicht ausgeführt werden, wenn der Schalter <a href="-robust.md"><strong>/robust</strong></a> angegeben ist.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2377"></span><span id="midl2377"></span><dl> <dt><strong>MIDL2377</strong></dt> </dl></td>
<td><dl> <dt><span id="conflicting_attributes_specified"></span><span id="CONFLICTING_ATTRIBUTES_SPECIFIED"></span>In Konfliktstehende Attribute angegeben</dt> <dd> Sowohl [<a href="context-handle-serialize.md"><strong>context_handle_serialize</strong></a>] als auch [<a href="context-handle-noserialize.md"><strong>context_handle_noserialize</strong></a>] wurden angegeben.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2378"></span><span id="midl2378"></span><dl> <dt><strong>MIDL2378</strong></dt> </dl></td>
<td><dl> <dt><span id="_serialize____noserialize__can_be_applied_to_context_handles"></span><span id="_SERIALIZE____NOSERIALIZE__CAN_BE_APPLIED_TO_CONTEXT_HANDLES"></span>[serialize], [noserialize] kann auf context_handles</dt> <dd> Die ACF-Attribute [context_handle_serialize] oder [context_handle_noserialize] können nur auf Typen angewendet werden, die Kontexthandles sind.<br/> IDL-Beispieldatei:<br/>
<pre class="syntax" data-space="preserve"><code>typedef /*[context_handle] */ void *PV;    //Note: PV is *not* a context handle.</code></pre>
ACF-Beispieldatei:<br/>
<pre class="syntax" data-space="preserve"><code>typedef [context_handle_serialize] PV;    //MIDL 2378</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2379"></span><span id="midl2379"></span><dl> <dt><strong>MIDL2379</strong></dt> </dl></td>
<td><dl> <dt><span id="The_compiler_reached_a_limit_for_a_format_string_representation._See_documentation_for_advice."></span><span id="the_compiler_reached_a_limit_for_a_format_string_representation._see_documentation_for_advice."></span><span id="THE_COMPILER_REACHED_A_LIMIT_FOR_A_FORMAT_STRING_REPRESENTATION._SEE_DOCUMENTATION_FOR_ADVICE."></span>Der Compiler hat einen Grenzwert für eine Formatzeichenfolgendarstellung erreicht. Weitere Informationen finden Sie in der Dokumentation.</dt> <dd> Der MIDL-Compiler hat einen Grenzwert von 64 KB für Formatzeichenfolgen. Dieser Fehler tritt im Allgemeinen auf, wenn IDL-Dateien andere IDL-Dateien enthalten. Die zusammengesetzte IDL-Datei, die von allen include-Anweisungen generiert wird, überschreitet die Grenzwerte der Typdarstellungstabellen des Interpreters der Marshalling-Engine. Versuchen Sie, die Importdirektive anstelle der include-Direktive in Ihren IDL-Dateien zu verwenden. Weitere Informationen finden Sie unter <a href="importing-system-header-files.md">Importieren von Systemheaderdateien,</a> <a href="include.md"><strong>Einschließen</strong></a>von und <a href="import.md"><strong>Importieren von</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2380"></span><span id="midl2380"></span><dl> <dt><strong>MIDL2380</strong></dt> </dl></td>
<td><dl> <dt><span id="wire_format_may_be_incorrect__you_may_need_to_use_-ms_conf_struct__see_documentation_for_advice"></span><span id="WIRE_FORMAT_MAY_BE_INCORRECT__YOU_MAY_NEED_TO_USE_-MS_CONF_STRUCT__SEE_DOCUMENTATION_FOR_ADVICE"></span>Das Wire-Format ist möglicherweise falsch. Möglicherweise müssen Sie -ms_conf_struct verwenden. Weitere Informationen finden Sie in der Dokumentation.</dt> <dd> Der MIDL-Compiler konnte kein transkonstantes Format für die Daten generieren. Eine gängige Möglichkeit, diesen Fehler zu erhalten, besteht darin, eine <strong>ms_conf_struct</strong> innerhalb einer komplexen Struktur zu definieren.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2381"></span><span id="midl2381"></span><dl> <dt><strong>MIDL2381</strong></dt> </dl></td>
<td><dl> <dt><span id="a_stack_size_or_an_offset_bigger_than_64_K_limit._See_documentation_for_advice."></span><span id="a_stack_size_or_an_offset_bigger_than_64_k_limit._see_documentation_for_advice."></span><span id="A_STACK_SIZE_OR_AN_OFFSET_BIGGER_THAN_64_K_LIMIT._SEE_DOCUMENTATION_FOR_ADVICE."></span>eine Stapelgröße oder einen Offset, der größer als der Grenzwert von 64 K ist. Weitere Informationen finden Sie in der Dokumentation.</dt> <dd> Der Aufruf führt zu einem Stapel, der größer als 64 KB ist. Versuchen Sie, die Daten in kleineren Blöcken zu übergeben.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2382"></span><span id="midl2382"></span><dl> <dt><strong>MIDL2382</strong></dt> </dl></td>
<td><dl> <dt><span id="an_interpreter_mode_forced_for_64-bit_platform_"></span><span id="AN_INTERPRETER_MODE_FORCED_FOR_64-BIT_PLATFORM_"></span>Ein Interpretermodus, der für die 64-Bit-Plattform erzwungen wird </dt> <dd> 64-Bit-Plattformen erfordern den Kompilierungsmodus /Oicf.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2383"></span><span id="midl2383"></span><dl> <dt><strong>MIDL2383</strong></dt> </dl></td>
<td><dl> <dt><span id="The_array_element_size_is_bigger_than_64_KB_limit."></span><span id="the_array_element_size_is_bigger_than_64_kb_limit."></span><span id="THE_ARRAY_ELEMENT_SIZE_IS_BIGGER_THAN_64_KB_LIMIT."></span>Die Größe des Arrayelements ist größer als der Grenzwert von 64 KB.</dt> <dd> Alle Arrayelemente müssen eine Größe von weniger als 64 KB aufweisen.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2384"></span><span id="midl2384"></span><dl> <dt><strong>MIDL2384</strong></dt> </dl></td>
<td><dl> <dt><span id="there_can_be_only_one__Icid__parameter_in_a_method__and_it_should_be_last_or_second_to_last_if_last_parameter_has__retval_"></span><span id="there_can_be_only_one__icid__parameter_in_a_method__and_it_should_be_last_or_second_to_last_if_last_parameter_has__retval_"></span><span id="THERE_CAN_BE_ONLY_ONE__ICID__PARAMETER_IN_A_METHOD__AND_IT_SHOULD_BE_LAST_OR_SECOND_TO_LAST_IF_LAST_PARAMETER_HAS__RETVAL_"></span>es kann nur einen [Icid]-Parameter in einer Methode geben, und er sollte der letzte oder der letzte sein, wenn der letzte Parameter [retval] hat.</dt> <dd> Ein Parameter mit dem Attribut [<a href="lcid.md"><strong>lcid</strong></a>] muss zuletzt auftreten. Die einzige Ausnahme ist, wenn auch ein Parameter mit dem Attribut [<a href="retval.md"><strong>retval</strong></a>] vorhanden ist. Wenn beides der Fall ist, muss der zweite bis letzte Parameter in der Parameterliste das Attribut [ <strong>lcid</strong>] aufweisen. Der letzte Parameter muss über das Attribut [<strong>retval</strong>] verfügen.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2385"></span><span id="midl2385"></span><dl> <dt><strong>MIDL2385</strong></dt> </dl></td>
<td><dl> <dt><span id="incorrect_syntax_for_midl_pragma"></span><span id="INCORRECT_SYNTAX_FOR_MIDL_PRAGMA"></span>Falsche Syntax für midl_pragma</dt> <dd> Der MIDL-Compiler hat einen unbekannten Syntaxfehler in einer midl_pragma-Anweisung erkannt.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2386"></span><span id="midl2386"></span><dl> <dt><strong>MIDL2386</strong></dt> </dl></td>
<td><dl> <dt><span id="__int3264_is_not_supported_in__osf_mode"></span><span id="__INT3264_IS_NOT_SUPPORTED_IN__OSF_MODE"></span>__int3264 wird im /osf-Modus nicht unterstützt.</dt> <dd> Wenn Sie __int3264 verwenden müssen, kompilieren Sie im Modus /ms-ext.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2387"></span><span id="midl2387"></span><dl> <dt><strong>MIDL2387</strong></dt> </dl></td>
<td><dl> <dt><span id="unresolved_symbol_in_type_library"></span><span id="UNRESOLVED_SYMBOL_IN_TYPE_LIBRARY"></span>Nicht aufgelöstes Symbol in der Typbibliothek</dt> <dd> Der Compiler konnte eine formale Deklaration oder einen Typ, auf den verwiesen wird, in der Typbibliothek nicht auflösen.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2388"></span><span id="midl2388"></span><dl> <dt><strong>MIDL2388</strong></dt> </dl></td>
<td><dl> <dt><span id="async_pipes_cannot_be_passed_by_value"></span><span id="ASYNC_PIPES_CANNOT_BE_PASSED_BY_VALUE"></span>Asynchrone Pipes können nicht als Wert übergeben werden</dt> <dd> Asynchrone Pipes sollten als Verweis oder adresse übergeben werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2389"></span><span id="midl2389"></span><dl> <dt><strong>MIDL2389</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_offset_exceed_64-KB_limit_for_interpreted_procedures"></span><span id="parameter_offset_exceed_64-kb_limit_for_interpreted_procedures"></span><span id="PARAMETER_OFFSET_EXCEED_64-KB_LIMIT_FOR_INTERPRETED_PROCEDURES"></span>Parameteroffset überschreitet 64-KB-Grenzwert für interpretierte Prozeduren</dt> <dd> Dieser Fehler bedeutet in der Regel, dass eine Prozedur zu viele Parameter aufweist.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2390"></span><span id="midl2390"></span><dl> <dt><strong>MIDL2390</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid_array_element"></span><span id="INVALID_ARRAY_ELEMENT"></span>Ungültiges Arrayelement</dt> <dd> Pipes können nicht als Arrayelemente verwendet werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2391"></span><span id="midl2391"></span><dl> <dt><strong>MIDL2391</strong></dt> </dl></td>
<td><dl> <dt><span id="dispinterface_members_must_be_methods__properties_or_interfaces"></span><span id="DISPINTERFACE_MEMBERS_MUST_BE_METHODS__PROPERTIES_OR_INTERFACES"></span>Dispinterface-Member müssen Methoden, Eigenschaften oder Schnittstellen sein.</dt> <dd> Eine Disp-Schnittstelle darf keine Typdefinitionen, Strukturen, Enumerationen oder Unions enthalten.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2392"></span><span id="midl2392"></span><dl> <dt><strong>MIDL2392</strong></dt> </dl></td>
<td><dl> <dt><span id="_local__procedure_without__call_as_"></span><span id="_LOCAL__PROCEDURE_WITHOUT__CALL_AS_"></span>[local]-Prozedur ohne [call_as]</dt> <dd> Objektprozesuren mit dem Attribut [<a href="local.md"><strong>local</strong></a>] erfordern auch das Attribut [<a href="call-as.md"><strong>call_as</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2393"></span><span id="midl2393"></span><dl> <dt><strong>MIDL2393</strong></dt> </dl></td>
<td><dl> <dt><span id="multi_dimensional_vector__switching_to__Oicf"></span><span id="multi_dimensional_vector__switching_to__oicf"></span><span id="MULTI_DIMENSIONAL_VECTOR__SWITCHING_TO__OICF"></span>Mehrdimensionaler Vektor, Wechseln zu /Oicf</dt> <dd> Der <a href="-os.md"><strong></strong></a> /Os-Optimierungsmodus unterstützt keine mehrdimensionalen, nicht fixierten Größenarrays. Der Compiler hat den Optimierungsmodus für diese Funktion automatisch in<strong>/Oicf</strong> umgeschaltet. <br/> Diese Warnung kann global unterdrückt werden, indem sie den Compilermodus ändert, indem Sie<strong>/Oicf</strong> in der MIDL-Befehlszeile angeben oder <strong>midl_pragma</strong> Warnung (deaktivieren: 2393) in der IDL-Datei verwenden. Der Optimierungsmodus kann für eine einzelne Funktion geändert werden, indem der Funktion in der ACF-Datei das<strong>[optimize( &quot; icf &quot; )</strong>]-Attribut hinzugefügt wird.<br/> Im folgenden Beispiel wird diese Warnung veranschaulicht:<br/>
<pre class="syntax" data-space="preserve"><code>void roo(long s1, [size_is(s1)] long a[][30];    //MIDL2393
void bar(long s1, long s2, [size_is(s1,s2) long **a);//MIDL2393</code></pre>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2395"></span><span id="midl2395"></span><dl> <dt><strong>MIDL2395</strong></dt> </dl></td>
<td><dl> <dt><span id="type_or_construct_not_supported_in_a_library_block_because_Oleaut32.dll_support_for_64-KB_polymorphic_types_is_missing"></span><span id="type_or_construct_not_supported_in_a_library_block_because_oleaut32.dll_support_for_64-kb_polymorphic_types_is_missing"></span><span id="TYPE_OR_CONSTRUCT_NOT_SUPPORTED_IN_A_LIBRARY_BLOCK_BECAUSE_OLEAUT32.DLL_SUPPORT_FOR_64-KB_POLYMORPHIC_TYPES_IS_MISSING"></span>Typ oder Konstrukt wird in einem Bibliotheksblock nicht unterstützt, da Oleaut32.dll Unterstützung für polymorphe Typen mit 64 KB fehlt.</dt> <dd> Die OLE-Automatisierung unterstützt keine polymorphen Typen (z. B. _int3264, INT_PTR usw.). Diese Typen verfügen über inkompatible Datendarstellungen zwischen 32-Bit- und 64-Bit-Plattformen. Der Remoteaufruf schlägt zur Laufzeit auf 64-Bit-Plattformen fehl.<br/>
<blockquote>
[!Note]<br />
Beachten Sie, dass ab Windows Release 2000 64-Bit-TLB-Dateien von OLE Automation unterstützt werden, indem 32-Bit-TLB-Informationen zur Laufzeit konvertiert werden. Daher wird von MIDL nur die 32-Bit-TLB-Generierung unterstützt.
</blockquote>
<br/> Wenn MIDL nur zum Generieren einer Headerdatei verwendet wird, unterdrückt der Schalter <a href="-notlb.md"><strong>/notlb</strong></a> die Generierung der TLB-Datei.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2396"></span><span id="midl2396"></span><dl> <dt><strong>MIDL2396</strong></dt> </dl></td>
<td><dl> <dt><span id="old_interpreter_code_being_generated_for_64b"></span><span id="OLD_INTERPRETER_CODE_BEING_GENERATED_FOR_64B"></span>Alter Interpretercode, der für 64b generiert wird</dt> <dd> Dieser Fehler ist veraltet. Wenn dieser Fehler angezeigt wird, melden Sie einen Fehler an Microsoft, der Ihre IDL-Dateien, ACF-Dateien und die vollständige MIDL-Befehlszeile angibt.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2397"></span><span id="midl2397"></span><dl> <dt><strong>MIDL2397</strong></dt> </dl></td>
<td><dl> <dt><span id="the_compiler_switch_is_not_supported_anymore"></span><span id="THE_COMPILER_SWITCH_IS_NOT_SUPPORTED_ANYMORE"></span>Der Compilerschalter wird nicht mehr unterstützt.</dt> <dd> Der angegebene Switch oder die angegebenen Switches werden nicht mehr unterstützt.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2398"></span><span id="midl2398"></span><dl> <dt><strong>MIDL2398</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_execute_MIDL_engine"></span><span id="cannot_execute_midl_engine"></span><span id="CANNOT_EXECUTE_MIDL_ENGINE"></span>MIDL-Engine kann nicht ausgeführt werden</dt> <dd> Ab version Windows 2000 (MIDL-Version 5.03.279) wird der MIDL-Compiler mit zwei ausführbaren Dateien implementiert: Midl.exe (Treiber) und Midlc.exe (Compiler-Engine). Dieser Fehler gibt an, dass die Midl.exe Midlc.exe nicht starten kann. Stellen Sie sicher, dass sich Midlc.exe im selben Verzeichnis wie Midl.exe befindet und dass es sich um dieselbe Version handelt.<br/> Der Fehler wurde möglicherweise durch kopieren Midl.exe verursacht, aber nicht durch Midlx.exe aus der neuesten Verteilung. Führen Sie <strong>midl</strong> und/oder <strong>midlc</strong> in der Befehlszeile ohne Parameter aus, um die Versionsnummer der ausführbaren Datei anzuzeigen.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2399"></span><span id="midl2399"></span><dl> <dt><strong>MIDL2399</strong></dt> </dl></td>
<td><dl> <dt><span id="bad_commands_from_driver"></span><span id="BAD_COMMANDS_FROM_DRIVER"></span>Ungültige Befehle des Treibers</dt> <dd> Ab version Windows 2000 (MIDL-Version 5.03.279) wird der MIDL-Compiler mit zwei ausführbaren Dateien implementiert: Midl.exe (Treiber) und Midlc.exe (Compiler-Engine). Dieser Fehler gibt an, dass die temporäre Datei, die zum Übergeben von Befehlen von Midl.exe an Midlc.exe verwendet wird, fehlt oder beschädigt ist. Stellen Sie sicher, dass sich Midlc.exe im selben Verzeichnis wie Midl.exe befindet und dass es sich um dieselbe Version handelt.<br/> Der Fehler kann durch den Versuch verursacht worden sein, Midlc.exe direkt auszuführen, oder durch Kopieren von Midl.exe, aber nicht Midlc.exe aus der neuesten Verteilung. Führen Sie <strong>midl</strong> und/oder <strong>midlc</strong> in der Befehlszeile ohne Parameter aus, um die Versionsnummer der ausführbaren Datei anzuzeigen.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2400"></span><span id="midl2400"></span><dl> <dt><strong>MIDL2400</strong></dt> </dl></td>
<td><dl> <dt><span id="for_ole_automation__optional_parameters_should_be_VARIANT_or_VARIANT__"></span><span id="for_ole_automation__optional_parameters_should_be_variant_or_variant__"></span><span id="FOR_OLE_AUTOMATION__OPTIONAL_PARAMETERS_SHOULD_BE_VARIANT_OR_VARIANT__"></span>Für die Ole-Automatisierung sollten optionale Parameter VARIANT oder VARIANT * sein.</dt> <dd> Die OLE-Automatisierung erfordert, dass alle [optionalen] Parameter vom Typ <strong>VARIANT</strong> oder <strong>VARIANT* sind.</strong><br/> Bei der OLE-Automatisierung kann die Verwendung von Nicht-VARIANT-Parametern dazu führen, dass der Aufruf zur Laufzeit fehlschlägt oder nicht definierte Daten für die [<a href="optional.md"><strong>optionalen</strong></a>] Parameter übergeben wird.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2401"></span><span id="midl2401"></span><dl> <dt><strong>MIDL2401</strong></dt> </dl></td>
<td><dl> <dt><span id="_defaultvalue__is_applied_to_a_non-VARIANT_and__optional_._Please_remove__optional_"></span><span id="_defaultvalue__is_applied_to_a_non-variant_and__optional_._please_remove__optional_"></span><span id="_DEFAULTVALUE__IS_APPLIED_TO_A_NON-VARIANT_AND__OPTIONAL_._PLEASE_REMOVE__OPTIONAL_"></span>[defaultvalue] wird auf nicht VARIANT und [optional] angewendet. Entfernen Sie [optional]</dt> <dd> Das [<a href="defaultvalue.md"><strong>defaultvalue</strong></a>] -Attribut impliziert [<a href="optional.md"><strong>optional</strong></a>]. Das [ <strong>optionale</strong>] -Attribut ist nicht erforderlich.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2402"></span><span id="midl2402"></span><dl> <dt><strong>MIDL2402</strong></dt> </dl></td>
<td><dl> <dt><span id="_optional__attribute_is_inapplicable_outside_of_a_library_block"></span><span id="_OPTIONAL__ATTRIBUTE_IS_INAPPLICABLE_OUTSIDE_OF_A_LIBRARY_BLOCK"></span>[optional] Das Attribut kann außerhalb eines Bibliotheksblocks nicht verwendet werden.</dt> <dd> Die durch das <a href="optional.md"><strong>[optional</strong></a>] -Attribut implizierte Funktionalität gilt nicht für Proxys, die für eine Schnittstelle außerhalb eines Bibliotheksblocks generiert werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2403"></span><span id="midl2403"></span><dl> <dt><strong>MIDL2403</strong></dt> </dl></td>
<td><dl> <dt><span id="The_data_type_of_the__Icid__parameter_must_be_long"></span><span id="the_data_type_of_the__icid__parameter_must_be_long"></span><span id="THE_DATA_TYPE_OF_THE__ICID__PARAMETER_MUST_BE_LONG"></span>Der Datentyp des [Icid]-Parameters muss lang sein.</dt> <dd> Die OLE-Automatisierung erfordert, dass Parameter mit dem Attribut [<strong>Icid</strong>] vom Typ <a href="long.md"><strong>long sein müssen.</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2404"></span><span id="midl2404"></span><dl> <dt><strong>MIDL2404</strong></dt> </dl></td>
<td><dl> <dt><span id="procedures_with__propput____propget__or__propref__can_t_have_more_than_one_required_parameter_after__optional__one"></span><span id="PROCEDURES_WITH__PROPPUT____PROPGET__OR__PROPREF__CAN_T_HAVE_MORE_THAN_ONE_REQUIRED_PARAMETER_AFTER__OPTIONAL__ONE"></span>Prozeduren mit [propput], [propget] oder [propref] dürfen nach [optional] nicht mehr als einen erforderlichen Parameter haben.</dt> <dd> Es darf nicht mehr als einen Parameter ohne [<a href="optional.md"><strong>optional</strong></a>] nach dem letzten Parameter mit [<strong>optional</strong>] geben, wenn [<a href="propput.md"><strong>propput</strong></a>], [<a href="propget.md"><strong>propget</strong></a>] oder [ <a href="propputref.md"><strong>propputref</strong></a>] verwendet wird.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2405"></span><span id="midl2405"></span><dl> <dt><strong>MIDL2405</strong></dt> </dl></td>
<td><dl> <dt><span id="_comm_status__or__fault_status__with_pickling_requires_-Oicf"></span><span id="_comm_status__or__fault_status__with_pickling_requires_-oicf"></span><span id="_COMM_STATUS__OR__FAULT_STATUS__WITH_PICKLING_REQUIRES_-OICF"></span>[comm_status] oder [fault_status] mit Auswahl erfordert -Oicf</dt> <dd> Der alte Optimierungsmodus –<strong>Oi</strong> unterstützt keine Prozeduren oder Parameter mit [ <a href="comm-status.md"><strong>comm_status</strong></a>] oder [ <a href="fault-status.md"><strong>fault_status</strong></a>] mit Pickling (d. h. mit [ <a href="encode.md"><strong>encode</strong></a>] und/oder [ <a href="decode.md"><strong>decode</strong></a>]).<br/> Diese Warnung kann global unterdrückt werden, indem -<strong>Oicf</strong> in der MIDL-Befehlszeile oder für eine einzelne Funktion angegeben wird, indem der Funktion in der ACF-Datei das Attribut [optimize( &quot; icf:)] hinzugefügt wird.<br/> Im Allgemeinen wird der<strong>Oicf-Optimierungsmodus</strong> im<strong>Oi-Modus</strong> empfohlen.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2406"></span><span id="midl2406"></span><dl> <dt><strong>MIDL2406</strong></dt> </dl></td>
<td><dl> <dt><span id="midl_driver_and_compiler_version_mismatch"></span><span id="MIDL_DRIVER_AND_COMPILER_VERSION_MISMATCH"></span>Midl-Treiber und Compilerversionskonflikt</dt> <dd> Ab version Windows 2000 (MIDL-Version 5.03.279) wird der MIDL-Compiler mithilfe von zwei ausführbaren Dateien implementiert: Midl.exe (Treiber) und Midlc.exe (Compiler-Engine). Dieser Fehler gibt an, dass die Version Midl.exe nicht mit der Version von Midlc.exe.<br/> Der Fehler wurde möglicherweise durch das Kopieren Midl.exe, aber nicht durch Midlc.exe der neuesten Verteilung verursacht. Führen <strong>Sie midl</strong> und/oder <strong>midlc</strong> in der Befehlszeile ohne Parameter aus, um die Versionsnummer der ausführbaren Datei zu sehen.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2407"></span><span id="midl2407"></span><dl> <dt><strong>MIDL2407</strong></dt> </dl></td>
<td><dl> <dt><span id="no_intermediate_file_specified__use_Midl.exe"></span><span id="no_intermediate_file_specified__use_midl.exe"></span><span id="NO_INTERMEDIATE_FILE_SPECIFIED__USE_MIDL.EXE"></span>keine Zwischendatei angegeben: Verwenden Sie Midl.exe</dt> <dd> Ab version Windows 2000 (MIDL-Version 5.03.279) wird der MIDL-Compiler mithilfe von zwei ausführbaren Dateien implementiert: Midl.exe (Treiber) und Midlc.exe (Compiler-Engine). Dieser Fehler gibt an, Midlc.exe direkt ausgeführt wurde, anstatt Midl.exe.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2408"></span><span id="midl2408"></span><dl> <dt><strong>MIDL2408</strong></dt> </dl></td>
<td><dl> <dt><span id="processing_problem_with_a_parameter_in_a_procedure"></span><span id="PROCESSING_PROBLEM_WITH_A_PARAMETER_IN_A_PROCEDURE"></span>Verarbeitungsproblem mit einem Parameter in einer Prozedur</dt> <dd> Dieser Fehler kann beim Importieren von Daten aus einem TLB und bei einem ungültigen Parameter einer Prozedur angezeigt werden. <br/> Wenn dieser Fehler angezeigt wird, melden Sie einen Fehler an Microsoft. Geben Sie Ihre IDL-Dateien, ACF-Dateien, die TLB-Datei und die vollständige MIDL-Befehlszeile an.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2409"></span><span id="midl2409"></span><dl> <dt><strong>MIDL2409</strong></dt> </dl></td>
<td><dl> <dt><span id="processing_problem_with_a_field_in_a_structure"></span><span id="PROCESSING_PROBLEM_WITH_A_FIELD_IN_A_STRUCTURE"></span>Verarbeitungsproblem mit einem Feld in einer Struktur</dt> <dd> Dieser Fehler kann beim Importieren von Daten aus einem TLB und bei einer Struktur mit einer ungültigen Struktur oder einem ungültigen Union-Feld angezeigt werden.<br/> Wenn dieser Fehler angezeigt wird, melden Sie einen Fehler an Microsoft. Geben Sie Ihre IDL-Dateien, ACF-Dateien, die TLB-Datei und die vollständige MIDL-Befehlszeile an.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2410"></span><span id="midl2410"></span><dl> <dt><strong>MIDL2410</strong></dt> </dl></td>
<td><dl> <dt><span id="internal_compiler_inconsistency_detected__the_format_string_offset_is_invalid._See_the_documentation_for_more_information."></span><span id="internal_compiler_inconsistency_detected__the_format_string_offset_is_invalid._see_the_documentation_for_more_information."></span><span id="INTERNAL_COMPILER_INCONSISTENCY_DETECTED__THE_FORMAT_STRING_OFFSET_IS_INVALID._SEE_THE_DOCUMENTATION_FOR_MORE_INFORMATION."></span>Interne Compilerinkonsistenz erkannt: Der Formatzeichenfolgenoffset ist ungültig. Weitere Informationen finden Sie in der Dokumentation.</dt> <dd> Der MIDL-Compiler hat einen ungültigen Wert in seinen internen Datenstrukturen erkannt. Dies kann durch rekursive Strukturen oder durch einen Compiler verursacht werden, der seine eigenen Grenzwerte für die Darstellung interner Daten verletzt. Um das Problem zu identifizieren und/oder zu beheben, versuchen Sie, die IDL-Datei zu vereinfachen. Hierzu können Sie komplexe Parameter und rekursive Datenstrukturen vereinfachen oder die IDL-Datei verkleinern, indem Sie sie aufteilen. Diese Meldung kann von einem Diagnosedruck mit zusätzlichen Informationen zum Problem begleitet werden.<br/> Wenn dieser Fehler angezeigt wird, melden Sie einen Fehler an Microsoft. Geben Sie Ihre IDL-Dateien, ACF-Dateien, die vollständige MIDL-Befehlszeile und gegebenenfalls die Diagnoseausgabe an.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2411"></span><span id="midl2411"></span><dl> <dt><strong>MIDL2411</strong></dt> </dl></td>
<td><dl> <dt><span id="internal_compiler_inconsistency_detected__the_type_offset_is_invalid._See_the_documentation_for_more_information."></span><span id="internal_compiler_inconsistency_detected__the_type_offset_is_invalid._see_the_documentation_for_more_information."></span><span id="INTERNAL_COMPILER_INCONSISTENCY_DETECTED__THE_TYPE_OFFSET_IS_INVALID._SEE_THE_DOCUMENTATION_FOR_MORE_INFORMATION."></span>Interne Compilerinkonsistenz erkannt: Der Typoffset ist ungültig. Weitere Informationen finden Sie in der Dokumentation.</dt> <dd> Der MIDL-Compiler hat einen ungültigen Wert in seinen internen Datenstrukturen erkannt. Dies kann durch rekursive Strukturen oder durch einen Verstoß des Compilers an seine eigenen Grenzwerte für die Darstellung interner Daten verursacht werden. Um das Problem zu identifizieren und/oder zu beheben, versuchen Sie, die IDL-Datei zu vereinfachen. Hierzu können Sie komplexe Parameter und rekursive Datenstrukturen vereinfachen oder die IDL-Datei verkleinern, indem Sie sie aufteilen. Diese Meldung kann von einem Diagnosedruck mit zusätzlichen Informationen zum Problem begleitet werden.<br/> Wenn dieser Fehler angezeigt wird, melden Sie einen Fehler an Microsoft. Geben Sie Ihre IDL-Dateien, ACF-Dateien, die vollständige MIDL-Befehlszeile und gegebenenfalls die Diagnoseausgabe an.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2412"></span><span id="midl2412"></span><dl> <dt><strong>MIDL2412</strong></dt> </dl></td>
<td><dl> <dt><span id="SAFEARRAY_roo__syntax_is_not_supported_outside_of_the_library_block__use_LPSAFEARRAY_for_proxy"></span><span id="safearray_roo__syntax_is_not_supported_outside_of_the_library_block__use_lpsafearray_for_proxy"></span><span id="SAFEARRAY_ROO__SYNTAX_IS_NOT_SUPPORTED_OUTSIDE_OF_THE_LIBRARY_BLOCK__USE_LPSAFEARRAY_FOR_PROXY"></span>SAFEARRAY(syntax)-Syntax wird außerhalb des Bibliotheksblocks nicht unterstützt. Verwenden Sie LPSAFEARRAY als Proxy.</dt> <dd> Explizit typierte SAFEARRAYs sind außerhalb eines Bibliotheksblocks nicht zulässig. Verwenden Sie stattdessen LPSAFEARRAY.<br/> Im folgenden Beispiel wird dieser Fehler veranschaulicht:<br/>
<pre class="syntax" data-space="preserve"><code>void roo(SAFEARRAY(long) *a); //MIDL2412 when outside a library block
void roo(LPSAFEAEEAY a);         //OK</code></pre>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2413"></span><span id="midl2413"></span><dl> <dt><strong>MIDL2413</strong></dt> </dl></td>
<td><dl> <dt><span id="bit_fields_are_not_supported"></span><span id="BIT_FIELDS_ARE_NOT_SUPPORTED"></span>Bitfelder werden nicht unterstützt.</dt> <dd> Bitfelder im C-Stil werden von MIDL nicht unterstützt. Dies gilt sowohl für die Proxygenerierung als auch für die TLB-Generierung.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2414"></span><span id="midl2414"></span><dl> <dt><strong>MIDL2414</strong></dt> </dl></td>
<td><dl> <dt><span id="floating_point_or_complex_return_types_with__decode__are_not_supported_in_-Oicf__using_-OI"></span><span id="floating_point_or_complex_return_types_with__decode__are_not_supported_in_-oicf__using_-oi"></span><span id="FLOATING_POINT_OR_COMPLEX_RETURN_TYPES_WITH__DECODE__ARE_NOT_SUPPORTED_IN_-OICF__USING_-OI"></span>Gleitkomma- oder komplexe Rückgabetypen mit [Decodierung] werden in -Oicf mit -OI nicht unterstützt.</dt> <dd> Prozeduren mit Gleitkomma- oder Struktur-/Union-Rückgabetypen werden in der Stilauswahl -Oicf nicht unterstützt. Bei 32-Bit-32-Bit ist die Verwendung des Optimierungsmodus -Oi beim Serialisieren von Daten (mithilfe von [Encode] und/oder [Decodierung]) ein Umweg. Da der alte Interpreter im Stil "-Oi" und die Auswahlunterstützung jedoch nach dem Release von Windows 2000 aus dem Weg gestrichen sind, wird die Verwendung von Zeigern dringend empfohlen, um dieses Problem zu beheben. Beachten Sie außerdem, dass das Ändern einer Schnittstellenmethode zur Verwendung eines [out, ref]-Zeigers anstelle des Rückgabewerts, der das Problem verursacht, in der Regel vollständig abwärtskompatibel ist und leicht von der App-Ebene ausgeblendet werden kann. <br/> Diese Warnung kann global unterdrückt werden, indem -Oi in der MIDL-Befehlszeile oder für eine einzelne Funktion angegeben wird, indem der Funktion in der ACF-Datei das Attribut [optimize( i )] hinzugefügt &quot; &quot; wird.<br/> Im folgenden Beispiel wird das Problem veranschaulicht:<br/> datei.idl: <br/>
<pre class="syntax" data-space="preserve"><code>double GetDouble();</code></pre>
datei.acf: <br/>
<pre class="syntax" data-space="preserve"><code>[decode] GetDouble();</code></pre>
Eine Möglichkeit, diese Einschränkung zu umgehen, besteht in der Übergeben eines [out]-Parameters, der das Ergebnis enthält, anstatt einen Rückgabewert zu verwenden:<br/> datei.idl: <br/>
<pre class="syntax" data-space="preserve"><code>void GetDouble([out] double *result); //top level pointer is a [ref] pointer</code></pre>
datei.acf: <br/>
<pre class="syntax" data-space="preserve"><code>[decode] GetDouble();</code></pre>
Wie bereits erwähnt, ist die oben beschriebene Lösung nicht nur für die neuen Schnittstellen, sondern auch als Problemumgehung für die alten Schnittstellen gut. Die Wire-Darstellung für das neue out-Argument ist mit der für den Rückgabewert identisch (beachten Sie &quot; void als neuen &quot; Rückgabewert).<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2415"></span><span id="midl2415"></span><dl> <dt><strong>MIDL2415</strong></dt> </dl></td>
<td><dl> <dt><span id="the_return_type_is_not_supported_for_64-bit_when_using__decode_"></span><span id="THE_RETURN_TYPE_IS_NOT_SUPPORTED_FOR_64-BIT_WHEN_USING__DECODE_"></span>Der Rückgabetyp wird bei Verwendung von [decode] für 64-Bit nicht unterstützt.</dt> <dd> Prozeduren mit Gleitkomma- oder Struktur-/Union-Rückgabetypen werden im 64-Bit-Modus bei der Datenserialisierung (mit [ <a href="encode.md"><strong>encode</strong></a>] und/oder [ <a href="decode.md"><strong>decode</strong></a>]) nicht unterstützt. Dies bezieht sich auf den alten Stil des Interpreters -Oi und das Datenseriierer, das auf der 64-Bit-Plattform nicht unterstützt wird. Weitere Informationen finden Sie in der Beschreibung von MIDL2414. <br/> Im folgenden Beispiel wird dieser Fehler veranschaulicht:<br/> datei.idl: <br/>
<pre class="syntax" data-space="preserve"><code>double GetDouble();</code></pre>
datei.acf: <br/>
<pre class="syntax" data-space="preserve"><code>[decode] GetDouble();</code></pre>
Folgendes wird als Arbeitsumgehung für neue und alte Schnittstellen empfohlen. Verwenden Sie einen [out]-Parameter, um das Ergebnis anstelle eines Rückgabewerts zu halten:<br/> datei.idl: <br/>
<pre class="syntax" data-space="preserve"><code>void GetDouble([out] double *result); //top level pointer is a [ref] pointer.</code></pre>
datei.acf: <br/>
<pre class="syntax" data-space="preserve"><code>[decode] GetDouble();</code></pre>
Beachten Sie, dass diese Lösung bei der Kabelverkabelung vollständig abwärtskompatibel ist, da die Wire-Darstellung eines [ref, out]-Zeigers oder eines Double-Zeigers mit der eines Double-Zeigers identisch ist.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2416"></span><span id="midl2416"></span><dl> <dt><strong>MIDL2416</strong></dt> </dl></td>
<td><dl> <dt><span id="transmitted_type_may_not_contain_a_full_pointer_for_either__wire_marshal__or__user_marshal_"></span><span id="TRANSMITTED_TYPE_MAY_NOT_CONTAIN_A_FULL_POINTER_FOR_EITHER__WIRE_MARSHAL__OR__USER_MARSHAL_"></span>Der übertragene Typ darf keinen vollständigen Zeiger für [wire_marshal] oder [user_marshal] enthalten.</dt> <dd> Typen mit <a href="wire-marshal.md"><strong>attributen</strong></a>[ wire_marshal ] oder [ <a href="user-marshal.md"><strong>user_marshal</strong></a>] dürfen keine vollständigen Zeiger ([ <strong>ptr</strong>]) enthalten. Verwenden Sie stattdessen [ <a href="unique.md"><strong>unique</strong></a>] oder [ <a href="ref.md"><strong>ref</strong></a>].<br/> Im folgenden Beispiel wird dieser Fehler veranschaulicht:<br/>
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
<td><dl> <dt><span id="transmitted_type_must_either_be_a_pointer_or_have_a_constant_size_for__wire_marshal__and__user_marshal_"></span><span id="TRANSMITTED_TYPE_MUST_EITHER_BE_A_POINTER_OR_HAVE_A_CONSTANT_SIZE_FOR__WIRE_MARSHAL__AND__USER_MARSHAL_"></span>Der übertragene Typ muss entweder ein Zeiger sein oder eine konstante Größe für [wire_marshal] und [user_marshal] haben.</dt> <dd> Typen der obersten Ebene mit attributen [ <a href="wire-marshal.md"><strong>wire_marshal</strong></a>] oder [ <a href="user-marshal.md"><strong>user_marshal</strong></a>] müssen zur Kompilierzeit eine klar definierte Größe haben. Sie dürfen keine konformen Arrays oder Arrays unterschiedlicher Größe sein oder enthalten.<br/> Im folgenden Beispiel wird dieser Fehler veranschaulicht:<br/>
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
<td><dl> <dt><span id="procedures_with__propget__must_have_at_least_one_parameter_or_a_return_value"></span><span id="PROCEDURES_WITH__PROPGET__MUST_HAVE_AT_LEAST_ONE_PARAMETER_OR_A_RETURN_VALUE"></span>Prozeduren mit [propget] müssen mindestens einen Parameter oder einen Rückgabewert haben.</dt> <dd> Prozeduren mit dem [propget]-Attribut müssen über eine Möglichkeit verfügen, den Eigenschaftswert zurück zu geben. Sie müssen mindestens einen<a href="-out.md"><strong>[out]-Parameter</strong></a>oder einen Rückgabewert haben.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2461"></span><span id="midl2461"></span><dl> <dt><strong>MIDL2461</strong></dt> </dl></td>
<td><dl> <dt><span id="The__readonly__attribute_was_applied_at_the_method_level."></span><span id="the__readonly__attribute_was_applied_at_the_method_level."></span><span id="THE__READONLY__ATTRIBUTE_WAS_APPLIED_AT_THE_METHOD_LEVEL."></span>Das [readonly]-Attribut wurde auf Methodenebene angewendet.</dt> <dd> Das [readonly]-Attribut kann nur auf Parameterebene angewendet werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2465"></span><span id="midl2465"></span><dl> <dt><strong>MIDL2465</strong></dt> </dl></td>
<td><dl> <dt><span id="Structures_containing_conformant_arrays_must_be_passed_by_reference"></span><span id="structures_containing_conformant_arrays_must_be_passed_by_reference"></span><span id="STRUCTURES_CONTAINING_CONFORMANT_ARRAYS_MUST_BE_PASSED_BY_REFERENCE"></span>Strukturen, die konforme Arrays enthalten, müssen als Verweis übergeben werden.</dt> <dd> Parameter der obersten Ebene in RPC müssen zur Kompilierzeit eine klar definierte Größe haben. Sie dürfen weder ein konformes Array noch ein Array unterschiedlicher Größe enthalten. Darüber hinaus können Benutzer einen Typ ohne klar definierte Größe nicht codieren/decodieren. Anwendungen müssen konforme Strukturen bzw. konforme unterschiedliche Strukturen als Verweis übergeben.<br/> Im folgenden Beispiel wird dieser Fehler veranschaulicht:<br/>
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
<td><dl> <dt><span id="_internal_compiler_problem__system_error_code__-_the_compiler_cannot_continue_for_an_unknown_reason._See_documentation_for_a_workaround."></span><span id="_internal_compiler_problem__system_error_code__-_the_compiler_cannot_continue_for_an_unknown_reason._see_documentation_for_a_workaround."></span><span id="_INTERNAL_COMPILER_PROBLEM__SYSTEM_ERROR_CODE__-_THE_COMPILER_CANNOT_CONTINUE_FOR_AN_UNKNOWN_REASON._SEE_DOCUMENTATION_FOR_A_WORKAROUND."></span> Internes <system error code> - Compilerproblem, das der Compiler aus einem unbekannten Grund nicht fortsetzen kann. Eine Problemumgehung finden Sie in der Dokumentation.</dt> <dd> Der Compiler konnte nicht fortgesetzt werden, und die Ursache des Fehlers ist unbekannt. Die hexadezimale Fehlernummer ist ein Systemfehlerbezeichner. Die Kompilierung ist möglicherweise aufgrund eines externen Problems fehlgeschlagen, z. B. aufgrund einer Nicht genügend Arbeitsspeicherbedingung. In diesem Fall finden Sie weitere Informationen in Winerror.h oder Ntstatus.h. <br/> Es gibt zwei Situationen, in denen dieser Fehler normalerweise generiert wird:<br/>
<ul>
<li>Der MIDL-Compiler konnte nach dem Erkennen eines Fehlers in der IDL-Datei nicht wiederhergestellt werden. Wenn MIDL Fehlermeldungen zu Ihrer IDL-Datei zurückgegeben hat, versuchen Sie, sie zu beheben und neu zu kompilieren. Wenn keine Fehlermeldungen angezeigt werden, ist der Compiler möglicherweise fehlgeschlagen, bevor er einen Fehler melden konnte. Suchen Sie in der Zeile, für die der interne Compilerfehler gemeldet wird, nach einem Syntaxfehler.</li>
<li>Der MIDL-Compiler konnte unter einer angegebenen Optimierungsoption keinen richtigen Code generieren. Versuchen Sie, die Compilermodi zu ändern, die Optimierung im gemischten Modus<a href="-os.md"><strong>(/Os)</strong></a>zu kompilieren oder alle Optimierungen zu entfernen. Oder kompilieren Sie mithilfe des Flags /NO_FORMAT_OPT, um die Standardoptimierung von Prozedur- und Typdeskriptoren durch MIDL zu unterdrücken.</li>
</ul>
Gelegentlich tritt dieser Fehler auch dann auf, wenn die IDL-Datei korrekt ist und keine Optimierungsoptionen verwendet werden. Wenn dies der Fall ist, versuchen Sie, den Codeabschnitt in der Nähe des Orts neu zu schreiben, an dem der Fehler gemeldet wurde, indem Sie kürzlich vorgenommene Änderungen entfernen, Datentypen vereinfachen oder neu angeordnet, Prototypen ändern oder andernt beginnen, Teile der IDL-Datei auskommentiert, um den Problemcode zu finden.<br/> Wenn keine dieser Optionen funktioniert oder Sie der Meinung sind, dass das Problem mit einem Fehler in Midl.exe zusammenhing, benachrichtigen Sie Microsoft, und geben Sie alle relevanten Details an.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



 

